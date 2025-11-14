FROM node:25.2-bullseye-slim@sha256:83a89bd0f971d5101293f5e723d6c6647a899cba824ea0341e1daa786cae0ad7 as node-base


FROM node-base as node-http-auth
ARG NODE_APP=.
ARG NODE_APP_NAME=http-service/server
# Add an env to save ARG
ENV NODE_APP_PATH "/app/${NODE_APP_NAME}"
COPY "$NODE_APP" /app
# Dont use exec form to interpolate correctly
CMD node $NODE_APP_PATH
