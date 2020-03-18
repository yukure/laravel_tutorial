FROM php:7.4-fpm-alpine3.11

RUN apk upgrade --update && \
    apk --no-cache add icu-dev autoconf make g++ gcc oniguruma-dev

RUN docker-php-ext-install pdo_mysql opcache mbstring