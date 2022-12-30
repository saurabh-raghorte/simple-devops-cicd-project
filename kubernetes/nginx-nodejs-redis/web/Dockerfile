FROM node:14.17.3-alpine3.14
WORKDIR /usr/src/app
COPY kubernetes/nginx-nodejs-redis/web/package*.json ./
RUN npm ci
COPY kubernetes/nginx-nodejs-redis/web/server.js ./
CMD ["npm","run","start"]
