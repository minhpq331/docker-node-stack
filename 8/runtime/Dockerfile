# minhpq331/node-stack:8-runtime
FROM node:8-alpine

MAINTAINER minhpq331@gmail.com

EXPOSE 3000

ARG NODE_ENV
ENV NODE_ENV $NODE_ENV

WORKDIR /app

# Copy code from builder image
ONBUILD COPY --from=builder /app .
ONBUILD ADD . /app
ONBUILD RUN yarn build

# Add build tag
ONBUILD ARG GIT_COMMIT_TAG=default
ONBUILD ENV GIT_COMMIT_TAG $GIT_COMMIT_TAG

CMD ["npm", "run", "docker:start"]