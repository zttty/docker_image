FROM python

#下面开始运行命令，此处更改Ubuntu的源为国内163的源RUN 
RUN apt-get -qq update \
 && apt-get -qq install --no-install-recommends \
    net-tools \
    vim \
    openssh-server 

#设置用于ssh连接的root密码
RUN echo 'root:123456'|chpasswd
RUN mkdir -p /var/run/sshd
#允许root连接
# RUN sed -i 's/PermitRootLogin without-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
RUN sed -i 'N;4a\PermitRootLogin yes' /etc/ssh/sshd_config
EXPOSE  22
CMD ["/usr/sbin/sshd", "-D"]