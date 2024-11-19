FROM php:8.3-fpm

RUN docker-php-ext-install -j$(nproc) pdo pdo_mysql
RUN apt-get update && \
    apt-get install --no-install-recommends -y git wget unzip && \
    wget -q https://getcomposer.org/download/2.8.3/composer.phar -O /usr/local/bin/composer && \
    chmod a+x /usr/local/bin/composer

