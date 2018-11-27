FROM php:7.2-fpm

MAINTAINER Masaki Obata <willow710kut@gmail.com>

RUN apt-get update \
 && apt-get install -y \
    git \
    zip \
    unzip \
    vim \
    iputils-ping \
    net-tools \
    openssl \
    libpng-dev \
    gnupg \
    mysql-client \
 && docker-php-ext-install pdo_mysql \
 && curl -sL https://deb.nodesource.com/setup_10.x | bash - \
 && apt-get install -y nodejs

RUN curl -sS https://getcomposer.org/installer | php \
 && mv composer.phar /usr/local/bin/composer \
 && curl -sL https://deb.nodesource.com/setup_10.x | bash -

COPY ./ /var/www

WORKDIR /var/www
