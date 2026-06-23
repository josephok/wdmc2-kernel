FROM docker.io/library/debian:trixie as builder

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y \
        git build-essential vim \
        bc dialog sudo \
        libncurses5 libncurses-dev libmpc-dev \
        libmpfr-dev libgmp3-dev \
        flex bison debootstrap debian-keyring debian-archive-keyring qemu-user-static \
        u-boot-tools kmod gcc-arm-linux-gnueabihf && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /build

VOLUME /build
