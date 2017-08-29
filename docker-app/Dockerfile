FROM node:7.8.0

ENV NPM_CONFIG_LOGLEVEL warn

COPY . .

RUN npm run build

RUN apt-get update \
    && apt-get install nginx




EXPOSE 3000