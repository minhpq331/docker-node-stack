# minhpq331/node-stack:8-builder
FROM node:8-alpine

MAINTAINER minhpq331@gmail.com

WORKDIR /app

RUN apk --no-cache add \
    g++ make python git \
    && yarn global add node-gyp \
    && rm -rf /var/cache/apk/*

ONBUILD ADD package.json yarn.lock /app/
ONBUILD RUN yarn --pure-lockfile