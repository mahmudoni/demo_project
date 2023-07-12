#Using 8.2 PHP Laravel image as the base
FROM php:8.2

# Install system dependencies
RUN apt-get update && apt-get install -y git unzip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

#Working directory is set in the container
WORKDIR /var/www/html

#Copy the Laravel project files to the container
COPY /app2/src/ /var/www/html

#Install PHP dependencies
RUN composer install

#Expose port 80 for the web server
EXPOSE 80

#Set the entrypoint to start the webserver
CMD ["php", "artisan", "serve", "--host", "0.0.0.0", "--port", "80"]
