# Arguments needed during image build.
# * TZ - required; timezone, e.g. Europe/Warsaw
# * JAVA_MAJOR_VERSION - required; Java major release, e.g. 17

FROM ubuntu:focal

ARG TZ
ARG JAVA_MAJOR_VERSION

USER root
WORKDIR /root

# Set timezone so that we don't get asked during apt install.
RUN set -eux; \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install Java.
RUN set -eux; \
    apt update -y; \
    apt install -y openjdk-$JAVA_MAJOR_VERSION-jdk; \
    apt-get clean