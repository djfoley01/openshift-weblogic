FROM registry.access.redhat.com/rhel7:latest
MAINTAINER Johnathan Kupferer <jkupfere@redhat.com>

ENV JAVA_VERSION=${JAVA_VERSION:-1.8.0} \
    JAVA_TYPE=${JAVA_TYPE:-oracle}

ENV JAVA_HOME=/usr/lib/jvm/java-${JAVA_VERSION}-${JAVA_TYPE}
COPY java-1.8.0-oracle-devel-1.8.0.172-3.el7.x86_64.rpm /java-1.8.0-oracle-devel-1.8.0.172-3.el7.x86_64.rpm
COPY java-1.8.0-oracle-1.8.0.172-3.el7.x86_64.rpm /java-1.8.0-oracle-1.8.0.172-3.el7.x86_64.rpm
COPY java-1.8.0-oracle-headless-1.8.0.172-3.el7.x86_64.rpm /java-1.8.0-oracle-headless-1.8.0.172-3.el7.x86_64.rpm

RUN yum install -y \
      /java-1.8.0-oracle-headless-1.8.0.172-3.el7.x86_64.rpm \
      /java-1.8.0-oracle-1.8.0.172-3.el7.x86_64.rpm \
      /java-1.8.0-oracle-devel-1.8.0.172-3.el7.x86_64.rpm && \
    yum clean all

RUN rm -rf /var/cache/yum
