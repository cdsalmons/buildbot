# This example docker file show how to customize the base slave docker
# to add build dependencies to build the python+nodejs buildbot_travis package

FROM        slave
MAINTAINER  Buildbot maintainers

# Install required npm packages
RUN apt-get install -y python-software-properties software-properties-common  && \
    add-apt-repository -y ppa:chris-lea/node.js && \
    apt-get update

RUN apt-get install -y -o APT::Install-Recommends=false -o APT::Install-Suggests=false \
    nodejs git libmysqlclient-dev
