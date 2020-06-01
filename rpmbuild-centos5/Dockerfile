FROM centos:5.11

# Disable fastestmirror, replace urls to vault
RUN sed -i 's|mirror.centos.org/centos/$releasever|vault.centos.org/5.11|g' /etc/yum.repos.d/*.repo && \
	sed -i 's|^mirrorlist|#mirrorlist|g' /etc/yum.repos.d/*.repo && \
	sed -i 's|^#baseurl|baseurl|g' /etc/yum.repos.d/*.repo && \
	sed -i 's|enabled=1|enabled=0|g' /etc/yum/pluginconf.d/fastestmirror.conf

RUN yum update -y

RUN yum install -y gcc gcc-c++ \
                   libtool libtool-ltdl \
                   make cmake \
                   git \
                   pkgconfig \
                   sudo \
                   automake autoconf \
                   yum-utils rpm-build && \
    yum clean all
