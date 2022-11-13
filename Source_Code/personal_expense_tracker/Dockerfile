FROM node:16.6.2-alpine as build-step

WORKDIR /app
ENV PATH /app/node_modules/.bin:$PATH
COPY package.json /app/
COPY package-lock.json /app/
COPY nginx.conf ./app/
COPY ./src ./app/src
COPY ./public ./app/public
RUN npm install
RUN npm run build

FROM nginx:1.17.10-alpine
COPY --from=build-stage /app/build/ /usr/share/nginx/html
# Copy the default nginx.conf provided by tiangolo/node-frontend
COPY --from=build-stage /nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 3000
