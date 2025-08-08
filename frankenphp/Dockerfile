FROM dunglas/frankenphp:php8.2.29

# 开发:
RUN cp $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini

COPY --from=composer:2.8.10 /usr/bin/composer /usr/bin/composer