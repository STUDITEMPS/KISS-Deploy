FROM quay.io/sameersbn/gitlab-ci-multi-runner:latest
MAINTAINER Andreas Guth <andreas.guth@studitemps.de>

USER root

RUN apt-get update && \
    apt-get install -y lxc python-pip apt-transport-https ca-certificates
RUN pip install docker-compose
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
RUN echo deb https://apt.dockerproject.org/repo ubuntu-trusty main > /etc/apt/sources.list.d/docker.list
RUN apt-get update && apt-get install docker-engine

VOLUME /home/gitlab_ci_multi_runner/data

