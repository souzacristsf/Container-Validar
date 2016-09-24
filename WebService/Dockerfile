FROM ubuntu:16.04

MAINTAINER Michel Ferreira Souza

RUN apt-get update -y

# utilizando esse comando para construir
# docker build -t codecasts/webserver .

RUN apt-get install -y apache2 php libapache2-mod-php

RUN rm /var/www/html/index.html # esse comando exclui o arquivo do apache

ADD start.sh /root/start.sh

RUN chmod +x /root/start.sh

# isso permite que eu rode assim no terminal -> docker run -it --rm -p 8080:80 codecasts/webserver - liberando a porta local
EXPOSE 80

# isso permite que eu rode assim no terminel -> docker run -it --rm codecasts/webserver /bin/bash
CMD ["/root/start.sh"]
