FROM seanmccann/rails-dockerfiles:alpine3.11

RUN apk --update-cache add --virtual build-dependencies mariadb-dev
RUN apk add --update mysql-client

ADD ../Gemfile* ./
ADD ../package.json ./


RUN gem install mysql2 -v0.5.3
RUN bundle install --jobs=`expr $(cat /proc/cpuinfo | grep -c "cpu cores") - 1` --retry 3
RUN yarn && yarn cache clean

RUN apk del build-dependencies