FROM ubuntu:latest

LABEL Backend="studentapp microservice"

ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz /opt/

WORKDIR /opt/

RUN apt update && \
    apt install unzip java-11-openjdk -y && \
    unzip apache-tomcat-9.0.93.tar.gz /opt/

COPY 
