FROM ubuntu:bionic
MAINTAINER gad.maor@gmail.com

RUN apt-get update \
 && apt-get install -y -q --no-install-recommends \
    autokey-gtk \
    python3-pip \
    python3-setuptools \
    git \
    virtualenv \
    build-essential \
    python3-dev \
    libdbus-glib-1-dev \
    libgirepository1.0-dev \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN pip3 install \
    autokey \
    PyQt5 \
    qscintilla

RUN groupadd -g 1001 gadm && useradd -u 1000 -g gadm -m gadm
RUN chown -R gadm:gadm /home/gadm
USER gadm
WORKDIR /home/gadm
ENV QT_X11_NO_MITSHM 1

CMD ["autokey-qt"]
