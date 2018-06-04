From php:7.2.6-fpm-stretch
RUN apt-get update && apt-get install -yq zlib1g-dev libpng-dev libxml2-dev
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ && docker-php-ext-install -j$(nproc) gd
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install zip
RUN docker-php-ext-install opcache
RUN docker-php-ext-install xml
RUN pecl install apcu && docker-php-ext-enable apcu