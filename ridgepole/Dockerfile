FROM ruby:alpine

COPY Gemfile /ridgepole/
WORKDIR /ridgepole

RUN apk add --no-cache --virtual .build build-base \
  && apk add --no-cache postgresql-dev \
  && cd /ridgepole \
  && bundle install \
  && rm -rf /ridgepole \
  && rm -rf /usr/local/bundle/cache \
  && apk del --no-cache .build

CMD ["ridgepole"]