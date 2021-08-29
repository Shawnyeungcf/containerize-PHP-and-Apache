# ARG for setting the specific php version
ARG PHP_VERSION=""

# Image from docker hub
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine

# Update the system inside docker
RUN apk upgrade;