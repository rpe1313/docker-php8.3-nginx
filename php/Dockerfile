FROM php:8.3-fpm

# Always latest 8.3.x because the base tag is floating

COPY www.conf /usr/local/etc/php-fpm.d/www.conf

RUN mkdir -p /var/run/php \
    && chown nobody:nogroup /var/run/php \
    && chmod 755 /var/run/php

# Default command is already php-fpm
