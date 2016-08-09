FROM php:7.0.8-apache

WORKDIR /var/www

RUN curl -sS https://getcomposer.org/installer | php
RUN ./composer.phar create-project block8/phpci phpci --keep-vcs --no-dev
RUN cd phpci && ../composer.phar install
RUN ./console phpci:install