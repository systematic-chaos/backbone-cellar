FROM centos:7

MAINTAINER Germán Moltó - gmolto@dsic.upv.es

RUN yum -y update && \
    yum -y install \
    httpd \
    php \
    php-mysql

COPY src/ /var/www/html

RUN sed -i s/None/All/g /etc/httpd/conf/httpd.conf

EXPOSE 80

ENTRYPOINT ["apachectl", "-DFOREGROUND"]
