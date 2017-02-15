FROM php:5-apache
#COPY www/ /var/www/html
RUN a2enmod rewrite
RUN docker-php-ext-install mysqli mysql
RUN apt-get update && apt-get -y install mc

RUN echo "date.timezone = Europe/Moscow" >> /usr/local/etc/php/php.ini

#ADD site1.conf /etc/apache2/sites-enabled/

RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/bin/ --filename=composer