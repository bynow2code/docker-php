FROM php:8.1-fpm-alpine3.21

RUN apk update && apk add --no-cache nginx supervisor tzdata

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions redis pdo_mysql xdebug

COPY --from=composer /usr/bin/composer /usr/bin/composer
