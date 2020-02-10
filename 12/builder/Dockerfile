# minhpq331/node-stack:10-builder
FROM node:12-alpine

MAINTAINER minhpq331@gmail.com

WORKDIR /app

RUN apk --no-cache add \
    g++ make python git \
    && yarn global add node-gyp \
    && rm -rf /var/cache/apk/*

ONBUILD ADD package.json yarn.lock /app/
ONBUILD RUN yarn --pure-lockfile

ONBUILD ADD . /app
ONBUILD RUN yarn build
ONBUILD RUN yarn --pure-lockfile --prod