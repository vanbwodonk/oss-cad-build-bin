FROM lopsided/archlinux-arm64v8

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN date

COPY entrypoint.sh /entrypoint.sh

USER root

ENTRYPOINT ["/entrypoint.sh"]
