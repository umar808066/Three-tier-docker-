FROM ubuntu:latest

LABEL DEVOPSENGG="UMAR"

RUN apt update 
RUN apt install unzip apache2 -y
RUN rm -rf /var/www/html/index.html

WORKDIR /var/www/html 

COPY . /var/www/html

EXPOSE 81

CMD ["apachectl", "-D", "FOREGROUND"]

