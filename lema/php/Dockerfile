FROM php:8.1-fpm
RUN mkdir -p /app/files && \
    chown www-data:www-data /app/files && \
    apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
            libzip-dev \
            zip \
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
      && docker-php-ext-install gd pdo_mysql zip

# Copy your custom PHP configuration file into the container
COPY uploads.ini /usr/local/etc/php/conf.d/

# Ensure the PHP-FPM service uses the updated configuration
RUN chmod 644 /usr/local/etc/php/conf.d/uploads.ini