FROM nginx

RUN useradd christopher

WORKDIR /usr/share/nginx/html

COPY startbootstrap-agency-gh-pages .

ENV archivo=docker      

RUN echo "${archivo}" > ./env.html

EXPOSE 90

LABEL version="1"

USER christopher

RUN echo "yo soy $(whoami)" > /tmp/yo.html

USER root

RUN cp  /tmp/yo.html ./docker.html

VOLUME /var/log/nginx

CMD nginx -g 'daemon off;' 