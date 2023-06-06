FROM ubuntu:22.04
ENV REGION Europe

RUN apt-get update
RUN apt-get install -y iputils-ping
RUN apt-get install -y python3 python3-pip 
RUN apt-get install -y ansible
RUN mkdir -p /etc/ansible
RUN apt-get update
RUN apt-get upgrade -y
