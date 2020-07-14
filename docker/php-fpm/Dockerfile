FROM php:7.2-fpm

ENV DEBIAN_FRONTEND noninteractive

RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
vim

RUN apt-get update \
    && apt-get install -y libpq-dev \
    && docker-php-ext-install pdo_mysql pdo_pgsql

RUN curl -SL https://deb.nodesource.com/setup_13.x | bash
RUN apt-get install -y nodejs && \
    npm install -g npm@latest && \
    npm install -g @vue/cli

WORKDIR /var/www/html

# RUN apt-get update && apt-get install -y git zlib1g-dev zip unzip
# RUN docker-php-ext-install zip

# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

# WORKDIR /var/www/html

# RUN composer install
# RUN php artisan key:generate