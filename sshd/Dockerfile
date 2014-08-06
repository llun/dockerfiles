From debian
MAINTAINER Maythee Anegboonlap "null@llun.in.th"

ADD https://ftp-master.debian.org/keys/archive-key-7.0.asc /tmp/key.asc
RUN cat /tmp/key.asc | apt-key add -
ADD sources.list /etc/apt/

RUN apt-get update
RUN apt-get install -y openssh-server git vim aptitude wget
RUN mkdir /var/run/sshd

ADD sshd_config /etc/ssh/

RUN echo 'root:password' | chpasswd

RUN mkdir -p /usr/local/etc/init.d/
ADD start.sh /usr/local/etc/init.d/
RUN chmod a+x /usr/local/etc/init.d/start.sh

CMD ["/usr/local/etc/init.d/start.sh"]
