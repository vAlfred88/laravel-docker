FROM node:alpine

WORKDIR /usr/src/app

ADD ./docker/laravel-echo-server/ .

RUN yarn

EXPOSE 3000
CMD [ "npm", "start", "--force" ]
