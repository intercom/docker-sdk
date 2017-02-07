# This is a comment
FROM ubuntu:16.04
#RUN apt-get update && apt-get install nodejs && apt-get install npm
RUN apt-get update && apt-get install -y \
  build-essential \
  curl \
  git \
  vim \
  nodejs \
  npm

#RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN ln -s /usr/bin/nodejs /usr/bin/node && npm install intercom-client \
  gulp \
  gulp-babel \
  babel-preset-es2015
  
RUN mkdir -p /intercom/mount_dir
WORKDIR /intercom

RUN git clone https://github.com/intercom/example-node.git

