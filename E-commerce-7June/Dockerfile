FROM php:apache

COPY apache-config.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite

CMD ["apache2-foreground"]

