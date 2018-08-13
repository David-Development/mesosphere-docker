FROM ubuntu:16.04

RUN echo 'Europe/Berlin' > /etc/timezone && rm /etc/localtime && dpkg-reconfigure -f noninteractive tzdata

# Install dependancies
#RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF
RUN    apt-get -y update \
    && apt-get -y install curl python-setuptools python-pip python-dev python-protobuf lsb-release \
    && rm -rf /var/lib/apt/lists/*

RUN DISTRO=$(lsb_release -is | tr '[:upper:]' '[:lower:]'); CODENAME=$(lsb_release -cs); echo "deb http://repos.mesosphere.io/${DISTRO} ${CODENAME} main" | tee /etc/apt/sources.list.d/mesosphere.list

