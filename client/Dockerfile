FROM node:14-alpine AS build

WORKDIR /app

ENV PORT=5000

COPY  package*.json ./

RUN yarn install 

COPY . . /app/

EXPOSE ${PORT}

CMD [ "node","app.js" ]