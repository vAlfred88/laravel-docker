FROM php:fpm

RUN apt-get update

RUN apt-get install -qq git curl libmcrypt-dev libjpeg-dev libpng-dev libfreetype6-dev
RUN apt-get install -qq libbz2-dev libpq-dev zip libzip-dev exiftool imagemagick libmagickwand-dev

RUN apt-get clean

RUN docker-php-ext-install pdo pdo_pgsql pdo_mysql zip gd exif
RUN pecl install imagick
RUN docker-php-ext-enable imagick gd pdo_mysql

#RUN curl -sL https://deb.nodesource.com/setup_12.x | bash
RUN curl --silent --show-error https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
#
#RUN apt-get install -qq nodejs

WORKDIR /var/www/

ADD ./www/ .

RUN chmod 777 /var/www/storage/

RUN COMPOSER_MEMORY_LIMIT=-1 composer install

EXPOSE 9000
