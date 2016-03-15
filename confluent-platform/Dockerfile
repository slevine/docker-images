# Builds a base docker image for the Confluent stream platform. It doesn't
# start up any particular service, just installs the platform. Other images
# inherit from this image to start up a particular service.
FROM nimmis/java:oracle-8-jdk

ENV SCALA_VERSION="2.11.7"
ENV JAVA_VERSION="8"
ENV CONFLUENT_MAJOR_VERSION="2.1"

RUN wget -qO - http://packages.confluent.io/deb/2.1/archive.key | apt-key add - && \
    add-apt-repository "deb http://packages.confluent.io/deb/2.1 stable main" && \
    apt-get update && \
    apt-get install -y confluent-platform-${SCALA_VERSION}
