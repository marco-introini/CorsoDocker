FROM php:8.0-apache

ARG TARGETPLATFORM

RUN echo "Immagine Docker per $TARGETPLATFORM"

RUN apt-get update && apt-get install -y \
    zip \
    unzip \
    curl \
    runit

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

WORKDIR /var/www/html/

RUN a2enmod rewrite
RUN a2enmod headers
RUN a2enmod ssl
RUN a2enmod include
RUN a2enmod expires
RUN a2enmod actions
RUN a2enmod status
RUN a2enmod info

EXPOSE 80

RUN apachectl start
