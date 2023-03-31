FROM php:8.1-fpm

RUN apt-get update && apt-get install -y supervisor

WORKDIR /var/www

RUN mkdir -p /var/log/supervisor

COPY ./docker/php/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

CMD ["/usr/bin/supervisord", "-n", "-c",  "/etc/supervisor/supervisord.conf"]
