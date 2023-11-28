# build
FROM node:16.20.2-alpine as build-step
RUN mkdir /app
# RUN npm cache clear --force
# WORKDIR /app
COPY ./front/dist /app

# nginx
FROM nginx:alpine
# COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./front/dist /usr/share/nginx/html
EXPOSE 80
STOPSIGNAL SIGTERM

CMD ["nginx", "-g", "daemon off;"]
