FROM ubuntu:20.10

ENV QT_VERSION v5.15.2
ENV QT_CREATOR_VERSION v4.14.2

# Build prerequisites
RUN apt-get -y update && apt-get -y install qtbase5-dev \
	libxcb-xinerama0-dev \
	build-essential \
	python

# Other useful tools
RUN apt-get -y update && apt-get -y install tmux \
	wget \
	zip \
	git \
	vim

# Simple root password in case we want to customize the container
RUN echo "root:root" | chpasswd

RUN useradd -G video -ms /bin/bash user

RUN mkdir -p /qt/build

WORKDIR /qt/build

ADD build_qt.sh ./build_qt.sh
RUN QT_VERSION=$QT_VERSION QT_CREATOR_VERSION=$QT_CREATOR_VERSION /qt/build/build_qt.sh

USER user

WORKDIR /qt

CMD ["bash"]
