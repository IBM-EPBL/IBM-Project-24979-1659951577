FROM node:16.6.2-alpine as build-step

WORKDIR /app
ENV PATH /app/node_modules/.bin:$PATH
COPY package.json ./
COPY package-lock.json ./
COPY ./src ./src
COPY ./public ./public
RUN npm install
EXPOSE 3000

CMD [ "npm", "start" ]
