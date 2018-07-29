FROM centos

LABEL version="1.0"
LABEL descripicion="imagen de tutorial"

RUN yum install httpd -y

WORKDIR /var/www/html

COPY startbootstrap-sb-admin-2-gh-pages . 
#ADD startbootstrap-sb-admin-2-gh-pages /var/www/html

ENV contenido=prueba

RUN echo "${contenido}" > ./prueba.html

#EXPOSE 81

RUN echo "$(whoami)" > ./user1.html
RUN useradd christopher
USER christopher
RUN echo "$(whoami)" > /tmp/user2.html
USER root
RUN cp  /tmp/user2.html ./user2.html

COPY run.sh /run.sh

CMD sh /run.sh