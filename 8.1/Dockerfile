FROM ubuntu:22.04

ARG PHP_VERSION

RUN apt-get update && apt-get install wget curl cron tzdata -y

RUN apt-get install $PHP_VERSION $PHP_VERSION-common $PHP_VERSION-mysql $PHP_VERSION-opcache \
    $PHP_VERSION-curl $PHP_VERSION-imagick $PHP_VERSION-redis $PHP_VERSION-memcached $PHP_VERSION-intl -y

