FROM php:7.4.27-fpm

RUN apt-get update && apt-get install -y

RUN docker-php-ext-install pdo pdo_mysql \
  && docker-php-ext-enable pdo pdo_mysql

RUN docker-php-ext-install opcache \
  &&  docker-php-ext-enable opcache

RUN docker-php-ext-install bcmath \
  && docker-php-ext-enable bcmath

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

CMD ["php-fpm"]