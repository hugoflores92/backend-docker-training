FROM nginx:stable-alpine

COPY nginx.conf /etc/nginx

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data

RUN rm /etc/nginx/conf.d/default.conf

CMD ["nginx"]

WORKDIR /var/www

EXPOSE 80 443