FROM ubuntu:xenial
MAINTAINER gad.maor@gmail.com

RUN apt-get update \
 && apt-get install -y -q --no-install-recommends \
    vim \
    ca-certificates \
    build-essential \
    software-properties-common \
    python3 \
    python3-pip \
    python3-bs4 \
    python3-requests \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN groupadd -g 1001 gadm && useradd -u 1000 -g gadm -m gadm
RUN chown -R gadm:gadm /home/gadm
USER gadm
WORKDIR /home/gadm/python

CMD ["python3"]
