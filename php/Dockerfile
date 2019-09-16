FROM php:fpm-alpine

RUN apk upgrade --update && \
    apk --no-cache add icu-dev autoconf make g++ gcc

RUN docker-php-ext-install pdo_mysql opcache mbstring