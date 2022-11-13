FROM node:16.6.2-alpine

WORKDIR /app
COPY package.json ./
# COPY package-lock.json ./
COPY ./ ./
RUN npm i
CMD ["npm", "run", "start"]
