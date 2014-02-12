FROM flynn/busybox
MAINTAINER Jonathan Rudenberg <jonathan@titanous.com>

ADD https://github.com/coreos/etcd/releases/download/v0.2.0/etcd-v0.2.0-Linux-x86_64.tar.gz /tmp

RUN cd /tmp && \
    mv etcd-v0.2.0-Linux-x86_64/etcd etcd-v0.2.0-Linux-x86_64/etcdctl /bin && \
    rm -rf etcd.tar etcd-v0.2.0-Linux-x86_64

ENTRYPOINT ["/bin/etcd"]
