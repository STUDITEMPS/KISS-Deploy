FROM quay.io/sameersbn/gitlab-ci-multi-runner:latest
MAINTAINER Andreas Guth <andreas.guth@studitemps.de>

USER root

RUN apt-get update && \
    apt-get install -y lxc python-pip
RUN pip install docker-compose

VOLUME /home/gitlab_ci_multi_runner/data

