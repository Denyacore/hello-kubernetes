FROM node:16-alpine3.13

ARG IMAGE_CREATE_DATE
ARG IMAGE_VERSION
ARG IMAGE_SOURCE_REVISION

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install app dependencies
COPY ./src/app /usr/src/app/
# COPY ./src/app/package.json /usr/src/app/
RUN npm install

# Bundle app source
COPY . /usr/src/app

USER root

# Install curl
RUN apk --no-cache add curl


CMD [ "npm", "start" ]