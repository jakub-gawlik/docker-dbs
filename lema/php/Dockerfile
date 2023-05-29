FROM php:8.1-fpm
RUN apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
            libzip-dev \
            zip \
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
      && docker-php-ext-install gd pdo_mysql zip
