# Stage 1
FROM node:14 as build-stage

WORKDIR /bezkoder-ui
COPY package.json .
RUN npm install
COPY . .

ARG REACT_APP_API_BASE_URL
ENV REACT_APP_API_BASE_URL=$REACT_APP_API_BASE_URL

RUN npm run build

# Stage 2
EXPOSE $REACT_DOCKER_PORT
