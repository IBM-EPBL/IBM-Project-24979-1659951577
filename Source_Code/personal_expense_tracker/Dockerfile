FROM node:16.6.2-alpine

WORKDIR /app
COPY package.json ./
COPY package-lock.json ./
COPY ./src ./
COPY ./public ./
RUN npm i
EXPOSE 3000
CMD ["npm", "run", "start"]
