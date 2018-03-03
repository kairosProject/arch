FROM php:7.2-alpine

RUN mkdir /app
WORKDIR /app

ENTRYPOINT vendor/bin/codecept run --steps
