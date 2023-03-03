FROM ruby:2.6.5-alpine3.11

RUN apk --update-cache add --update --virtual build-dependencies \
  build-base \
  pcre-dev \
  ruby-dev

RUN gem install bundler -v 1.17.3
