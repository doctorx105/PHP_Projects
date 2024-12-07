# Use the official PHP image
FROM php:8.1-apache

# Install required extensions
RUN docker-php-ext-install mysqli && apt-get update && apt-get install -y libpng-dev && docker-php-ext-install gd

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Set working directory
COPY . /var/www/html

# Set permissions for files and directories in /var/www/html
RUN chown -R www-data:www-data /var/www/html
RUN find /var/www/html -type d -exec chmod 755 {} \;
RUN find /var/www/html -type f -exec chmod 644 {} \;

# Expose port 80
EXPOSE 80
