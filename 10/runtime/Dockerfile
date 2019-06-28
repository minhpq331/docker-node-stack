# minhpq331/node-stack:10-runtime
FROM node:10-alpine

MAINTAINER minhpq331@gmail.com

EXPOSE 3000

ARG NODE_ENV
ENV NODE_ENV $NODE_ENV

WORKDIR /app

ONBUILD COPY --from=builder /app .

# Add build tag
ONBUILD ARG GIT_COMMIT_TAG=default
ONBUILD ENV GIT_COMMIT_TAG $GIT_COMMIT_TAG

CMD ["npm", "run", "docker:start"]