FROM nginx:alpine
# RUN adduser -D myuser
RUN addgroup -g 61000 -S webuser &&\
    adduser -S -D -H  -u 61000 -h /var/cache/nginx -s /sbin/nologin -G webuser -g webuser webuser &&\
    touch /var/run/nginx.pid &&\
    chown -Rf webuser:webuser \
    /var/run/nginx.pid \
    /var/cache/nginx \
    /var/log/nginx

# COPY nginx.conf /etc/nginx/nginx.conf
USER webuser

CMD ["nginx", "-g", "daemon off;"]