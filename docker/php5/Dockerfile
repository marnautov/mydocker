FROM php:5-apache
RUN a2enmod rewrite
RUN a2enmod vhost_alias
RUN docker-php-ext-install mysqli mysql pdo pdo_mysql

RUN apt-get update && apt-get -y install mc wget

RUN echo "date.timezone = Europe/Moscow" >> /usr/local/etc/php/php.ini

RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/bin/ --filename=composer