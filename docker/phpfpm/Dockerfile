FROM php:7-fpm

RUN apt-get update && apt-get install -y \
  libjpeg-dev \
  libpng-dev

RUN docker-php-ext-install \
  gd \
  opcache \
  pdo_mysql

WORKDIR /srv/www
