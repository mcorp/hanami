FROM ruby:2.3-alpine

RUN apk add --update git \
  build-base \
  libxml2-dev \
  libxslt-dev \
  && rm -rf /var/cache/apk/*

RUN bundle config build.nokogiri --use-system-libraries

ENV HANAMI_VERSION 0.7.2

RUN gem install hanami --version "$HANAMI_VERSION"
