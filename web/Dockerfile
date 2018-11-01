FROM php:7.2-fpm

MAINTAINER Masaki Obata <willow710kut@gmail.com>

RUN apt-get update \
 && apt-get install -y \
    mysql-client \
    && docker-php-ext-install pdo_mysql

RUN apt-get install -y \
    git \
    zip \
    unzip \
    vim \
    iputils-ping \
    net-tools \
    openssl \
    libpng-dev

RUN curl -sS https://getcomposer.org/installer | php \
 && mv composer.phar /usr/local/bin/composer

RUN apt-get install -y gnupg \
 && curl -sL https://deb.nodesource.com/setup_10.x | bash - \
 && apt-get install -y nodejs

COPY ./ /var/www

WORKDIR /var/www
