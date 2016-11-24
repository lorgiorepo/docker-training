FROM node:argon

# File Author / Maintainer
MAINTAINER Lorgio Trinidad <lorgiotrinidad@gmail.com>

# create a directory for your app
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ENV REDIS_PORT_6379_TCP_ADDR 127.0.0.1
ENV REDIS_PORT_6379_TCP_PORT 6379

# install app dependencies
COPY package.json /usr/src/app
RUN npm install

# Budle app source
COPY . /usr/src/app

EXPOSE 8080
CMD ["npm", "start"]
