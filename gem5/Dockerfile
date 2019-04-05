FROM ubuntu:18.04
LABEL description='Build environment for gem5 Risc-V simulator.'

RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
        g++ \
        git \
        libgoogle-perftools-dev \
        libprotobuf-dev \
        m4 \
        protobuf-compiler \
        python \
        python-dev \
        scons \
        telnet \
        wget \
        zlib1g-dev \
        python3 \
        python3-dev
