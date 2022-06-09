# Arguments needed during image build.
# * JAVA_VERSION - required; Java major release, e.g. 17
# * TOMCAT_VERSION - required; Tomcat release, e.g. 9 or 10

ARG JAVA_VERSION

FROM hub.digpro.dev/java:${JAVA_VERSION}

ARG TOMCAT_VERSION

USER root
RUN mkdir /dps_build

WORKDIR /dps_build/

COPY tomcat${TOMCAT_VERSION}.tar.gz tomcat.tar.gz

RUN tar -xf tomcat.tar.gz && rm tomcat.tar.gz