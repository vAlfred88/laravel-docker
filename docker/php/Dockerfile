FROM php:7.3-fpm

ARG path

RUN apt-get update

RUN apt-get install -qq git curl libmcrypt-dev libjpeg-dev libpng-dev libfreetype6-dev
RUN apt-get install -qq libbz2-dev libpq-dev zip libzip-dev exiftool imagemagick libmagickwand-dev supervisor

RUN apt-get clean

RUN pecl install imagick xdebug

RUN docker-php-ext-install pdo pdo_mysql zip gd calendar
RUN docker-php-ext-enable pdo pdo_mysql zip gd calendar

RUN curl --silent --show-error https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/

EXPOSE 9000
