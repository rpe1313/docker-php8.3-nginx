# PHP 8.3 + Nginx Docker 
(IPv4 only, port 80, Unix socket, nobody:nogroup)

A minimal, production-oriented setup.

## Features

- Official `php:8.3-fpm` base (always latest 8.3.x on rebuild)
- Official `nginx:alpine`
- Listens **only on IPv4 port 80** (no IPv6), a proxy **MUST** be placed in front of this container if used for production or on the public internet
- PHP-FPM ↔ Nginx via Unix socket (`/var/run/php/php-fpm.sock`)
- Workers run as **nobody:nogroup**
