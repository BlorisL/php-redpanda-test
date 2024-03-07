FROM php:8.2-fpm-bullseye

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libwebp-dev \
    git \
    zip \
    unzip \
    libzip-dev \
    libxml2-dev \
    memcached \
    libmemcached-tools \
    iputils-ping \
    vim \
    git-flow \
    librdkafka-dev \
    && docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-configure gd --with-webp --with-jpeg --with-freetype \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install -j$(nproc) mysqli pdo pdo_mysql \
    && docker-php-ext-install -j$(nproc) zip \
    && docker-php-ext-install -j$(nproc) soap \
    && docker-php-ext-install -j$(nproc) sockets \
    && docker-php-ext-install -j$(nproc) pcntl \
    && docker-php-ext-install -j$(nproc) exif \
    && docker-php-ext-install -j$(nproc) intl

RUN pecl install rdkafka && docker-php-ext-enable rdkafka