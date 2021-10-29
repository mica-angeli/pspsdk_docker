FROM ubuntu:20.04

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=America/New_York
RUN apt update && \
    apt install -y sudo git autoconf automake bison bzip2 cmake doxygen flex gettext g++ gcc git gzip \
    libarchive-dev libcurl4-openssl-dev libelf-dev libgpgme-dev libncurses5-dev \
    libreadline-dev libssl-dev libtool-bin libusb-dev m4 make patch pkg-config \
    python3 python3-venv subversion tar tcl texinfo unzip wget xz-utils

WORKDIR /root/
RUN git clone https://github.com/pspdev/psptoolchain.git
WORKDIR /root/psptoolchain/
RUN ./toolchain-sudo.sh
