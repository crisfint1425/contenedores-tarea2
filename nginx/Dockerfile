FROM nginx:stable-alpine

# Directorio para archivos estáticos compartidos (wp-content de solo lectura)
RUN mkdir -p /var/www/html/wp-content && \
    chown -R nginx:nginx /var/www/html

# Página de healthz
RUN printf "OK\n" > /usr/share/nginx/html/healthz

# TLS opcional (si quisieras autosigned, coloca certs en ./nginx/certs)
# COPY certs /etc/nginx/certs

# Copia de confs se hace por volumen desde el host para facilitar iteración

