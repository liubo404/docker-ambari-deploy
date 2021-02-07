FROM centos:7.8.2003
MAINTAINER hope

# change yum repo
COPY Centos-7.repo /etc/yum.repos.d/CentOS-Base.repo


RUN yum install epel-release -y && yum clean all
RUN yum update -y && yum clean all


RUN yum install -y yum-utils yum-plugin-ovl tar git curl bind-utils unzip wget && yum clean all



# Setup sshd
RUN yum install -y openssh-server openssh-clients && yum clean all
RUN systemctl enable sshd

# initscripts (service wrapper for servicectl) is need othewise the Ambari is unable to start postgresql
RUN yum install -y initscripts && yum clean all



# install JDK8



