FROM node:alpine

WORKDIR /usr/src/app

ADD ./www/ .

RUN yarn

CMD ["npm", "run", "watch"]
