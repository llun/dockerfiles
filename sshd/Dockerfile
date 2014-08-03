From debian
MAINTAINER Maythee Anegboonlap "null@llun.in.th"

RUN apt-get update
RUN apt-get install -y openssh-server git vim
RUN mkdir /var/run/sshd

RUN echo 'root:password' | chpasswd

RUN mkdir -p /usr/local/etc/init.d/
ADD start.sh /usr/local/etc/init.d/
RUN chmod a+x /usr/local/etc/init.d/start.sh

EXPOSE 22
CMD ["/usr/local/etc/init.d/start.sh"]
