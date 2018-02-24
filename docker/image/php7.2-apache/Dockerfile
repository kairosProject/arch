FROM php:7.2-apache

RUN apt-get update
RUN apt-get install -y autoconf build-essential
RUN pecl install mongodb
RUN echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/mongodb.ini

RUN if [ ! -d "/var/www/html/app/cache" ]; then mkdir -p "/var/www/html/app/cache"; fi
RUN if [ ! -d "/var/www/html/app/log" ]; then mkdir -p "/var/www/html/app/log"; fi

RUN chown www-data:www-data /var/www/html/app/cache
RUN chmod 744 /var/www/html/app/cache
RUN chown www-data:www-data /var/www/html/app/log
RUN chmod 744 /var/www/html/app/log
