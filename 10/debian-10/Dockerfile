FROM docker.io/bitnami/minideb:buster
LABEL maintainer "Bitnami <containers@bitnami.com>"

COPY prebuildfs /
# Install required system packages and dependencies
RUN install_packages curl procps

ENV BITNAMI_APP_NAME="bitnami-shell" \
    BITNAMI_IMAGE_VERSION="10-debian-10-r188" \
    OS_ARCH="amd64" \
    OS_FLAVOUR="debian-10" \
    OS_NAME="linux"

RUN echo "nobody:x:1000:1000:nobody:/:/bin/sh" >> /etc/passwd
RUN echo "nobody:x:1000:" >> /etc/group
USER 1000
