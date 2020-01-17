FROM fedora:30
COPY root ./

RUN dnf install -y nginx \
        && dnf clean all \
        && rm -rf /var/cache/yum

CMD ["./entrypoint.sh"]
