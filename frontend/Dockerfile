FROM centos:7
LABEL APP="StudentappFE"
LABEL DevopsEngg="Mayur"


RUN yum install httpd -y
COPY index.html /var/www/html/index.html

EXPOSE 80
CMD httpd -DFOREGROUND