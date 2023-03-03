FROM ruby:2.7-alpine

RUN apk --update-cache add --update --virtual build-dependencies \
  build-base \
  pcre-dev \
  ruby-dev

RUN gem install bundler -v 1.17.3
