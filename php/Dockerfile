FROM php:7.4-fpm
RUN docker-php-ext-install pdo_mysql
RUN apt-get update && \
    apt-get -y install nginx && \
    apt-get -y install git && \
    apt-get -y install nodejs && \
    apt-get -y install npm
RUN npm install --global yarn
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
WORKDIR /var/www/norrahorse