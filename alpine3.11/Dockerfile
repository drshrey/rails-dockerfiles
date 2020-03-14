FROM ruby:2.6.5-alpine3.11

RUN apk --update-cache add --update --virtual build-dependencies \
  build-base \
  pcre-dev \
  ruby-dev

RUN apk add --update bash \
  ruby-nokogiri \
  nodejs-current \
  python2 \
  yaml \
  ruby-json \
  tzdata \
  ca-certificates \
  yarn && \
  rm -rf /var/cache/apk/*

RUN gem install bundler -v 1.17.3
