FROM ubuntu:16.04
RUN apt-get update && apt-get install -y \
  build-essential \
  curl \
  git \
  vim \
  nodejs \
  npm
RUN apt-get update && apt-get install -y curl \
  git \
  vim \ 
  php

RUN mkdir -p /intercom/mount_dir
WORKDIR /intercom
RUN curl -sS https://getcomposer.org/installer | php 

RUN php composer.phar require intercom/intercom-php
RUN git clone https://github.com/intercom/example-php.git 

