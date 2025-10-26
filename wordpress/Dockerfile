FROM wordpress:php8.2-fpm

# Opcional: extensiones útiles (gd, imagick si deseas)
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Ajustes de permisos mínimos para wp-content (volumen)
RUN usermod -u 1000 www-data && groupmod -g 1000 www-data

WORKDIR /var/www/html

# Salud mínima
HEALTHCHECK --interval=30s --timeout=5s --retries=5 CMD php -v || exit 1

