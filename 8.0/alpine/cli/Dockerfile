FROM spiritact/php-pgsql:8.0-cli-alpine3.16

RUN apk add --no-cache --virtual .build-deps autoconf g++ make

RUN pecl install redis && docker-php-ext-enable redis

RUN apk del .build-deps && rm -rf /tmp/* /var/vcache/apk/*
