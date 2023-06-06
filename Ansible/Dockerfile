FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install -y iputils-ping
RUN apt install -y python3 python3-pip
RUN apt-add-repository -y ppa:ansible/ansible
RUN apt install ansible -y
RUN apt-get update
RUN apt-get upgrade -y
