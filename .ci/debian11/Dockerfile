FROM debian:bullseye

# MAINTAINER DESY, Jan Kotanski <jankotan@gmail.com>

RUN apt-get -qq update && apt-get -qq -y dist-upgrade
RUN apt-get install -y g++  g++ doxygen git lsb-release libjs-mathjax fonts-mathjax fonts-mathjax-extras ghostscript libusb-dev graphviz make

RUN apt-get clean

# add p00user
RUN useradd -rm -d /home/p00user -s /bin/bash p00user
USER p00user
RUN mkdir -p /home/p00user/src
WORKDIR /home/p00user/src
