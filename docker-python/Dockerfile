FROM ubuntu:xenial
MAINTAINER gad.maor@gmail.com

RUN apt-get update \
 && apt-get install -y -q --no-install-recommends \
    ca-certificates \
    build-essential \
    python3 \
    python3-pip \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

USER root
WORKDIR /root

CMD ["/bin/bash"]
