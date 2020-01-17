FROM registry.access.redhat.com/ubi8/ubi-minimal
COPY root ./

RUN microdnf -y --setopt=tsflags=nodocs install nginx && \
    chmod 755 /etc/nginx/ssl && \
    microdnf clean all

CMD ["./entrypoint.sh"]
