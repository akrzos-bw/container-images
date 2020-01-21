FROM centos:7
COPY . .
### Install required packages
RUN yum -y --setopt=tsflags=nodocs install automake autotools bc epel-release \
        gcc git gnuplot libtool make openssh-clients patch net-tools && \
    yum -y --setopt=tsflags=nodocs install go stress && \
    mkdir -p build && cd build && \
    git clone https://github.com/jmencak/mb.git && \
      cd mb && make && cp ./mb /usr/local/bin && cd .. && \
    cd && rm -rf build && \
    yum remove automake autotools gcc go libtool make patch -y && \
    yum clean all
