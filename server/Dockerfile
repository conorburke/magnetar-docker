FROM node:10.8.0

# Create app directory
RUN mkdir -p /usr/src/magnetar
# RUN mkdir -p /usr/src/magnetar/client
WORKDIR /usr/src/magnetar

# Bundle app source
COPY . /usr/src/magnetar

# Install app dependencies
COPY package.json /usr/src/magnetar
COPY ./client/package.json /usr/src/magnetar/client
RUN yarn install && cd /usr/src/magnetar/client && yarn install

# # Bundle app source
# COPY . /usr/src/magnetar

# Build arguments
ARG NODE_VERSION=10.8.0

# Environment
ENV NODE_VERSION $NODE_VERSION