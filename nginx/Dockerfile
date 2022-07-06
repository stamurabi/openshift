FROM docker.io/library/nginx:stable-alpine

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./default.conf /etc/nginx/conf.d/default.conf

WORKDIR /app

## add permissions for nginx user
RUN mkdir /var/cache/nginx/client_temp
RUN chown -R nginx:root /app && chmod -R 755 /app && \
        chown -R nginx:root /var/cache/nginx && chmod -R g=u /var/cache/nginx && \
        chown -R nginx:root /var/log/nginx && chmod -R g=u /var/log/nginx && \
        chown -R nginx:root /etc/nginx/conf.d && chmod -R g=u /etc/nginx/conf.d
RUN touch /var/run/nginx.pid && \
        chown -R nginx:root /var/run/nginx.pid

USER nginx
