FROM rockylinux:9

RUN dnf install -y openssh-server python3 sudo procps-ng iproute net-tools && \
    ssh-keygen -A && \
    echo 'root:root' | chpasswd && \
    echo 'PermitRootLogin yes' >> /etc/ssh/sshd_config && \
    echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
