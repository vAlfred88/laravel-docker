FROM node:alpine

WORKDIR /usr/src/app

ADD ./patterneasy/ .

RUN yarn

CMD ["npm", "run", "watch"]
