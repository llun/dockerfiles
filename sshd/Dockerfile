From debian
MAINTAINER Maythee Anegboonlap "null@llun.in.th"

RUN apt-get update
RUN apt-get install -y openssh-server git vim
RUN mkdir /var/run/sshd

RUN echo 'root:password' | chpasswd

EXPOSE 22
