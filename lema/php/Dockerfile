FROM php:7.3-fpm
RUN apt-get update && apt-get install -y \
      libzip-dev \
      zip \
      libfreetype6-dev \
      libjpeg62-turbo-dev \
      libpng-dev \
&& docker-php-ext-configure zip --with-libzip \
&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
&& docker-php-ext-install zip pdo_mysql mysqli gd
