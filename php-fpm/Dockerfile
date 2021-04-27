FROM php:fpm-alpine

RUN addgroup -g 61000 -S webuser &&\
    adduser -S -D -H -u 61000 -s /sbin/nologin -G webuser -g webuser webuser &&\
    mkdir /sock &&\
    chown -R webuser:webuser /sock &&\
    docker-php-ext-install pdo_mysql opcache &&\
    docker-php-ext-enable pdo_mysql opcache
VOLUME [ "/sock" ]
USER webuser