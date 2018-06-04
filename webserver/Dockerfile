FROM ubuntu
RUN apt-get update
RUN apt-get -yq install apache2
RUN apt-get -yq install wget
RUN cd /tmp && wget http://mirrors.kernel.org/ubuntu/pool/multiverse/liba/libapache-mod-fastcgi/libapache2-mod-fastcgi_2.4.7~0910052141-1.2_amd64.deb && dpkg -i libapache2-mod-fastcgi_2.4.7~0910052141-1.2_amd64.deb; apt install -f
RUN a2enmod actions fastcgi alias proxy_fcgi
RUN a2enmod rewrite
ADD 000-default.conf /etc/apache2/sites-enabled
ENTRYPOINT ["apachectl", "-D", "FOREGROUND"]