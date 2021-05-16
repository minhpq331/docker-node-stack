# node-stack
Dockerfile for building and running nodejs app

Demo Dockerfile for each project:

```Dockerfile
FROM minhpq331/node-stack:12-builder as builder

FROM minhpq331/node-stack:12-runtime as runtime
```