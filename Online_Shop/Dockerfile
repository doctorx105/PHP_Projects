# # Use the official PHP image
# FROM php:8.1-apache

# # Install required extensions
# RUN docker-php-ext-install mysqli && apt-get update && apt-get install -y libpng-dev && docker-php-ext-install gd

# # Enable Apache mod_rewrite
# RUN a2enmod rewrite

# # Set working directory
# COPY . /var/www/html

# # Set permissions for files and directories in /var/www/html
# RUN chown -R www-data:www-data /var/www/html

# # Expose port 80
# EXPOSE 80

# Use the official PHP image
FROM php:8.1-apache

# Install required extensions
RUN docker-php-ext-install mysqli

# Enable mod_rewrite for Apache
RUN a2enmod rewrite

# Copy the application code to the container
COPY . /var/www/html

# Set permissions
RUN chown -R www-data:www-data /var/www/html

# Expose port 80
EXPOSE 80

# run in terminal docker-compose up -d --build
