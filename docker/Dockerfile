ARG PHP_TAG=6.0.1-php8.1-apache

FROM wordpress:${PHP_TAG}

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

# xdeugの設定にxdebug.iniを利用
COPY src/config/xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

CMD ["apache2-foreground"]