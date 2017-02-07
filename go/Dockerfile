# This is a comment
FROM ubuntu:14.04
#RUN apt-get update && apt-get install nodejs && apt-get install npm
RUN apt-get update && apt-get install -y \
  build-essential \
  curl \
  git \
  vim 

#RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN curl -O https://storage.googleapis.com/golang/go1.6.3.linux-amd64.tar.gz;\
  tar -xvf go1.6.3.linux-amd64.tar.gz; \
  mv go /usr/local; \
  mkdir /go_workspace

ENV PATH="/usr/local/go/bin:${PATH}" 
WORKDIR /go_workspace 
ENV GOPATH=/go_workspace 
RUN mkdir -p src/intercom/code/mount_dir;\
  go get gopkg.in/intercom/intercom-go.v2
WORKDIR src/intercom/code
RUN git clone https://github.com/intercom/example-go.git 
