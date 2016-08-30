FROM node:latest

# File Author / Maintainer
MAINTAINER Lorgio Trinidad <lorgiotrinidad@gmail.com>

# create a directory for your app
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# install app dependencies
COPY package.json /usr/src/app
RUN npm install

# Budle app source
COPY . /usr/src/app

EXPOSE 8080
CMD ["npm", "start"]
