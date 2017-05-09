FROM centos:latest

MAINTAINER Jeremy Utley "jerutley@gmail.com"

RUN yum clean all && yum -y update && yum -y install epel-release && yum -y --nogpgcheck install http://rpms.remirepo.net/enterprise/remi-release-7.rpm && yum -y install yum-utils && yum-config-manager --enable remi-php70

RUN yum -y install \
    php \
    php-bcmath \
    php-common \
    php-fpm \
    php-gd \
    php-imap \
    php-ldap \
    php-mbstring \
    php-mcrypt \
    php-mysqlnd \
    php-odbc \
    php-pdo \
    php-process \
    php-recode \
    php-snmp \
    php-tidy \
    php-xml \
    php-xmlrpc \
    php-opcache \
    php-pecl-apcu

ADD /php-fpm.conf /etc/php-fpm.conf

ADD /www.conf /etc/php-fpm.d/www.conf

RUN mkdir -p /srv/www

EXPOSE 9000

CMD ["/usr/sbin/php-fpm", "-F"]
