FROM node:16.20.2-alpine as build-step
RUN mkdir /app
RUN npm cache clear --force
WORKDIR /app
RUN npm install express nodemon
COPY ./server /app

EXPOSE 8000
STOPSIGNAL SIGTERM

CMD ["node", "server.js"]