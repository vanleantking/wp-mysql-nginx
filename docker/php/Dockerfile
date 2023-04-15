FROM php:8.1.18-fpm

RUN apt-get update && apt-get install -y zlib1g-dev g++ git libicu-dev zip libzip-dev acl procps \
    && docker-php-ext-install intl opcache pdo pdo_mysql \
    && pecl install apcu \
    && docker-php-ext-enable apcu \
    && docker-php-ext-configure zip \
    && docker-php-ext-install zip \
    && docker-php-ext-install mysqli
RUN apt-get install -y libcurl4-openssl-dev pkg-config libssl-dev

WORKDIR /var/www
