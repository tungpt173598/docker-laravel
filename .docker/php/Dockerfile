# Set master image
FROM php:8.1-fpm-alpine

# Set working directory
WORKDIR /var/www/html

# Install Additional dependencies
# Install PHP Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-enable pdo_mysql

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

# Copy existing application directory
COPY . .

