FROM php:8.1-alpine

RUN apk update && apk upgrade
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable pdo_mysql mysqli

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libonig-dev \
    build-essential \
    libzip-dev \
    libpng-dev \
    libjpeg62-turbo-dev \
    libwebp-dev libjpeg62-turbo-dev libpng-dev libxpm-dev \
    libfreetype6 \
    libmcrypt-dev \
    locales \
    zip \
    jpegoptim optipng pngquant gifsicle \
    vim \
    unzip \
    git \
    curl

RUN mv $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini

WORKDIR /var/www