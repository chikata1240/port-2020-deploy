FROM php:7.2-fpm

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y git zlib1g-dev zip unzip
RUN docker-php-ext-install zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
RUN composer global require hirak/prestissimo

WORKDIR /var/www/html