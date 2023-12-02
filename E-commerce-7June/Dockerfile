# Use an official PHP image as the base image
FROM php:7.4-apache

# Set the working directory in the container
WORKDIR /var/www/html

# Copy the application files to the container
COPY . .

# Install any additional dependencies your application might need
RUN apt-get update \
    && apt-get install -y \
        libzip-dev \
    && docker-php-ext-install zip

# Set up Apache configuration
COPY apache-config.conf /etc/apache2/sites-available/000-default.conf

# Expose port 80 for the web server
EXPOSE 80

# Start the Apache web server
CMD ["apache2-foreground"]

