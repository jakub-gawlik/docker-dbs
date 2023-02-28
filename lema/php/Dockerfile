FROM php:7.3-fpm
RUN apt-get update && apt-get install -y \
	libfreetype6-dev \
	libjpeg62-turbo-dev \
	libmcrypt-dev \
	libpng-dev \
	libbz2-dev \
	libcurl4-gnutls-dev \
	libxml2-dev \
	libssl-dev \
	libc-client-dev \
	libkrb5-dev \
	zlib1g-dev \
	libicu-dev \
	g++ \
	git \
	libsqlite3-dev \
	libpspell-dev \
	libreadline-dev \
	libedit-dev \
	librecode-dev \
	libsnmp-dev \
	libtidy-dev \
	libxslt1.1 \
	libxslt1-dev \
	ssmtp \
	snmp \
	libgmp-dev \
	libldb-dev \
	libldap2-dev \
	libsodium-dev \
	gnupg2 \
	wget \
	unzip \
	librabbitmq-dev \
	libaio1 \
	libzip-dev \
	zip \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ --with-png-dir=/usr/include/ \
	&& docker-php-ext-install -j$(nproc) gd \
	&& docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ \
	&& docker-php-ext-configure zip --with-libzip \
	&& docker-php-ext-configure imap --with-kerberos --with-imap-ssl \
	&& docker-php-ext-install -j$(nproc) imap \
	&& docker-php-ext-install ldap \
	&& docker-php-ext-install zip pdo_mysql mysqli
