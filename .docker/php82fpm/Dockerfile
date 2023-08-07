
FROM php:8.2-fpm

RUN pecl install xdebug
#    && docker-php-ext-enable xdebug \
#    && echo "xdebug.mode=debug" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
#    && echo "xdebug.client_host = host.docker.internal" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

COPY --from=composer /usr/bin/composer /usr/bin/composer
WORKDIR /var/www/html
RUN apt-get update && apt-get  install -y unzip git-core

RUN docker-php-ext-install pdo_mysql


#RUN composer install
