FROM node:14.17.3-alpine3.14

WORKDIR /usr/src/app

COPY nginx-nodejs-redis/web/package*.json ./
RUN npm ci
COPY nginx-nodejs-redis/web/server.js ./

CMD ["npm","start"]
