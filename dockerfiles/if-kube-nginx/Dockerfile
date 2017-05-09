FROM centos:latest

MAINTAINER Jeremy Utley "jerutley@gmail.com"

RUN yum clean all && yum -y update && yum -y install epel-release nginx

RUN ln -sf /dev/stdout /var/log/nginx/access.log  && ln -sf /dev/stderr /var/log/nginx/error.log && mkdir -p /srv/www

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
