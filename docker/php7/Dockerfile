FROM php:7.1-apache
RUN docker-php-ext-install mysqli

RUN apt-get update && apt-get install -y libssl-dev
RUN pecl install mongodb

RUN echo "extension=mongodb.so" > /usr/local/etc/php/conf.d/mongo.ini

RUN apt-get install -y zip git

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer