FROM ubuntu:16.04

# Install apt based dependencies required to run Rails as 
# well as RubyGems. As the Ruby image itself is based on a 
# Debian image, we use apt-get to install those.
RUN apt-get update && apt-get install -y \ 
  ruby \
  ruby-dev \ 
  ruby-bundler \
  build-essential \ 
  libcurl3-dev \
  curl \
  git \
  vim \ 
  nodejs

# Configure the main working directory. This is the base 
# directory used in any further RUN, COPY, and ENTRYPOINT 
# commands.
RUN mkdir -p /intercom
WORKDIR /intercom

RUN git clone https://github.com/intercom/example-ruby.git && mv -t . example-ruby/Gemfile* 
RUN gem install bundler && bundle install --jobs 20 --retry 5
