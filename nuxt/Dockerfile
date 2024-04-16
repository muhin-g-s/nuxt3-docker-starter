FROM node:18.20.2

ENV APP_ROOT /web

WORKDIR ${APP_ROOT}
ADD . ${APP_ROOT}

RUN npm install --package-lock
RUN npm ci

RUN npm run build
CMD node .output/server/index.mjs