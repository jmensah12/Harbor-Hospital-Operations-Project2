FROM docker.io/library/nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

RUN sed -i 's/listen       80;/listen       8080;/' /etc/nginx/conf.d/default.conf && \
    sed -i 's/listen  \[::\]:80;/listen  [::]:8080;/' /etc/nginx/conf.d/default.conf && \
    chmod -R g=u /var/cache/nginx /var/run /var/log/nginx /etc/nginx/conf.d

EXPOSE 8080