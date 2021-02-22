FROM centos

RUN yum install openssh-server -y

RUN yum install net-tools -y

RUN yum install passwd -y

RUN ssh-keygen -A

RUN echo redhat | passwd root --stdin

RUN cat /usr/sbin/sshd >> /etc/rc.d/rc.local

CMD ["/usr/sbin/sshd","-D"]
