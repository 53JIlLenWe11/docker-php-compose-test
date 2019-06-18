FROM php:7.2-fpm

WORKDIR /tmp

RUN apt update -y
RUN apt install -y git unzip
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer
RUN composer self-update
RUN composer global require hirak/prestissimo

RUN mkdir -p /www/html
VOLUME ["/www/html"]
WORKDIR /www/html

ENTRYPOINT ["composer"]
CMD ["--help"]
