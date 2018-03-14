FROM alpine:latest
LABEL maintainer="Chi Nguyen <chivitc1@gmail.com"
LABEL description="This example Dockerfile installs NGINX."
RUN apk add --update nginx && \
	rm -rf /var/cache/apk/* && \
	mkdir -p /tmp/nginx/
COPY files/nginx.conf /etc/nginx/nginx.conf
COPY files/default.conf /etc/nginx/conf.d/default.conf
ADD files/readme.txt.gz /usr/share/nginx/
COPY files/ /data
EXPOSE 80/tcp
ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]
