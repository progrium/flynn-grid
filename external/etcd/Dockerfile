FROM flynn/busybox
MAINTAINER Jonathan Rudenberg <jonathan@titanous.com>

ADD https://github.com/coreos/etcd/releases/download/v0.3.0/etcd-v0.3.0-linux-amd64.tar.gz /tmp/etcd.tar.gz

RUN cd /tmp && \
    tar xzf etcd.tar.gz && \
    mv etcd-v0.3.0-linux-amd64/etcd /bin && \
    rm -rf *etcd*

ENTRYPOINT ["/bin/etcd"]
