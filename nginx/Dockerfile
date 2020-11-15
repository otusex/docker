FROM centos:7


RUN yum install -y epel-release 
RUN yum install -y nginx 


WORKDIR /usr/share/nginx/html

COPY ./src/nginx.conf /etc/nginx/nginx.conf
COPY ./src/vhost.conf /etc/nginx/conf.d/vhost.conf

CMD [ "nginx", "-g", "daemon off;" ]
