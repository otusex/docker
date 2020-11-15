FROM centos:7


RUN    yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm \
    && yum -y install https://rpms.remirepo.net/enterprise/remi-release-7.rpm \
    && yum -y install yum-utils \
    && yum-config-manager --enable remi-php74 -y \
    && yum update -y \
    && yum -y install php-fpm \
    && mkdir -p /run/php-fpm/


WORKDIR /usr/share/nginx/html

COPY src/php-fpm.conf /etc/php-fpm.conf
COPY src/www.conf /etc/php-fpm.d/www.conf

CMD [ "php-fpm", "--fpm-config", "/etc/php-fpm.conf", "--nodaemonize"]

