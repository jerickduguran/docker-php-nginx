FROM php:7.3.0-fpm

ADD php.ini /usr/local/etc/php/conf.d/php.ini

RUN apt-get update \
  && docker-php-ext-install pdo_mysql mysqli mbstring

RUN apt-get update \
  && apt-get install -y libmemcached-dev zlib1g-dev \
  && pecl install memcached-3.1.3 \
  && docker-php-ext-enable memcached opcache