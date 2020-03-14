FROM seanmccann/rails-dockerfiles:latest

RUN apk --update-cache add postgresql-dev

ADD ../Gemfile* ./
ADD ../package.json ./

RUN bundle install --jobs=`expr $(cat /proc/cpuinfo | grep -c "cpu cores") - 1` --retry 3
RUN yarn && yarn cache clean

RUN apk del build-dependencies
