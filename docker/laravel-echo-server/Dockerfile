FROM node:alpine

WORKDIR /usr/src/app

ADD ./docker/laravel-echo-server/ .

RUN npm install -g laravel-echo-server

EXPOSE 6001

CMD ["npm", "start"]
