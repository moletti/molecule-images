ARG OS_RELEASE=focal

FROM ubuntu:${OS_RELEASE}

LABEL maintainer="Leo Moletti"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install  -y -q --no-install-recommends systemd systemd-sysv python python3 sudo bash ca-certificates iproute2  && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /lib/systemd/system/multi-user.target.wants/* \
    /etc/systemd/system/*.wants/* \
    /lib/systemd/system/local-fs.target.wants/* \
    /lib/systemd/system/sockets.target.wants/*udev* \
    /lib/systemd/system/sockets.target.wants/*initctl* \
    /lib/systemd/system/sysinit.target.wants/systemd-tmpfiles-setup* \
    /lib/systemd/system/systemd-update-utmp*

RUN systemctl set-default multi-user.target

VOLUME [ "/sys/fs/cgroup" ]

CMD ["/lib/systemd/systemd"]