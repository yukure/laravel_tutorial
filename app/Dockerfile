FROM php:7.4-fpm-alpine3.11

RUN apk upgrade --update && \
    apk --no-cache add icu-dev autoconf make g++ gcc oniguruma-dev
RUN docker-php-ext-install pdo_mysql opcache mbstring

# multi stage build
# https://docs.docker.com/develop/develop-images/multistage-build/#use-an-external-image-as-a-stage
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html

COPY . ./
RUN composer install