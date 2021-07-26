FROM php:7.3-fpm-alpine

RUN docker-php-ext-install pdo pdo_pgsql pdo_mysql zip gd exif calendar

COPY ./docker/cron/crontabs/crontab /etc/crontabs/root/

CMD ["crond", "-f"]