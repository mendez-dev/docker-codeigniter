# Utiliza una imagen base de PHP con Apache
FROM php:7.4-apache

# Habilita el módulo rewrite de Apache
RUN a2enmod rewrite

# Instala las dependencias necesarias y habilita la extensión intl
RUN apt-get update && apt-get install -y \
    libicu-dev \
    && docker-php-ext-install intl

# Copia la configuración del virtual host
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

# Habilita la extensión mysqli para la conexión a la base de datos MariaDB
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Reinicia Apache para aplicar los cambios
CMD ["apache2-foreground"]
