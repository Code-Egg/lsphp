FROM ubuntu:22.04

ARG PHP_VERSION

RUN apt-get update && apt-get install wget curl tzdata -y

RUN wget -O - https://repo.litespeed.sh | bash

RUN apt update

RUN apt-get install $PHP_VERSION

#RUN apt-get install $PHP_VERSION $PHP_VERSION-common $PHP_VERSION-mysql $PHP_VERSION-opcache \
#    $PHP_VERSION-curl $PHP_VERSION-imagick $PHP_VERSION-redis $PHP_VERSION-memcached $PHP_VERSION-intl -y

RUN ln -s /usr/local/lsws/$PHP_VERSION/bin/php /usr/bin/php

RUN php --version

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
WORKDIR /var/www/vhosts/

EXPOSE 9000
CMD ["php"]