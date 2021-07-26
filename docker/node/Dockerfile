FROM node:alpine

WORKDIR /var/www

ADD ./www/ .

RUN npm install -g yarn

CMD ["yarn", "run"]
