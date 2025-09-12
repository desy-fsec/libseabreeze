FROM debian:bookworm

# MAINTAINER DESY, Jan Kotanski <jankotan@gmail.com>

# RUN /bin/bash -c 'echo "deb http://ftp.de.debian.org/debian bookworm main" > /etc/apt/sources.list.d/debian9de.list'
RUN apt-get update
RUN apt-get install -y base-passwd apt-utils dialog -y
RUN echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections
RUN apt-get -qq update && apt-get -qq install -y libterm-readline-gnu-perl software-properties-common coreutils gnupg2 procps curl apt-transport-https gnupg2 ca-certificates wget
# RUN curl -s http://repos.pni-hdri.de/debian_repo.pub.gpg  | gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/debian-hdri-repo.gpg --import
# RUN chmod 644 /etc/apt/trusted.gpg.d/debian-hdri-repo.gpg
# # RUN add-apt-repository "deb http://repos.pni-hdri.de/apt/debian bookworm main" -y
# RUN cd /etc/apt/sources.list.d && wget http://repos.pni-hdri.de/bookworm-pni-hdri.list
RUN apt-get -qq update && apt-get -qq -y dist-upgrade

RUN apt-get -qq update && apt-get  -y install g++ doxygen git lsb-release libjs-mathjax fonts-mathjax fonts-mathjax-extras ghostscript libusb-dev graphviz	       


RUN apt-get clean


# add p00user
RUN useradd -rm -d /home/p00user -s /bin/bash p00user
USER p00user
RUN mkdir -p /home/p00user/src
WORKDIR /home/p00user/src
