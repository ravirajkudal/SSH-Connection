FROM ubuntu:20.04

RUN apt-get update && \
	apt-get install -y openssh-server sudo && \
	mkdir /var/run/sshd

RUN useradd -m devops && \
	echo "devops:pass123" | chpasswd && \
	adduser devops sudo

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]