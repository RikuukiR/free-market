FROM php:8.3-fpm

# 必要なシステムパッケージをインストール
RUN apt-get update && apt-get install -y \
  libpq-dev \
  libzip-dev \
  zip \
  unzip \
  curl

# Composerをインストール
RUN curl -sS https://getcomposer.org/installer | php && \
  mv composer.phar /usr/local/bin/composer

# 必要なPHP拡張をインストール
RUN docker-php-ext-install pdo_mysql

WORKDIR /var/www