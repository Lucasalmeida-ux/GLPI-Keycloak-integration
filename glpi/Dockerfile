FROM php:8.0-apache
COPY . /var/www/html

RUN apt-get update && apt-get install -y libicu-dev libcurl4-gnutls-dev libpng-dev libjpeg-dev libfreetype6-dev libonig-dev && \
    docker-php-ext-configure gd --with-freetype --with-jpeg && \
    docker-php-ext-install curl fileinfo gd json mbstring mysqli session zlib simplexml xml intl && \
    chown -R www-data:www-data /var/www/html/
