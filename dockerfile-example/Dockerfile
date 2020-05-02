FROM nginx
COPY myserver.conf /etc/nginx/conf.d/
RUN apt-get update -y && \
    apt-get install -y iputils-ping && \
    apt-get install -y procps && \
    apt-get install -y dnsutils

EXPOSE 80 8080
STOPSIGNAL SIGTERM
CMD ["nginx", "-g", "daemon off;"]
