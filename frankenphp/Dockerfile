FROM dunglas/frankenphp:1.9.0-php8-alpine

# 在此处添加其他扩展：
# RUN install-php-extensions \
# 	pdo_mysql \
# 	gd \
# 	intl \
# 	zip \
# 	opcache

# COPY --from=composer /usr/bin/composer /usr/bin/composer

# 设置时区为上海（Asia/Shanghai）
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENV SERVER_NAME="127.0.0.1, 172.18.0.2"

# 开发:
RUN cp $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini