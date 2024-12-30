FROM mcr.microsoft.com/devcontainers/python:1-3.10-bookworm

RUN pip install uv
RUN pip install tensorflow[and-cuda]
RUN pip install jupyter

RUN apt-get update && apt-get install -y \
    wget \
    build-essential \
    autoconf \
    automake \
    libtool \
    libpcre3-dev \
    && apt-get clean

WORKDIR /tmp

RUN wget http://prdownloads.sourceforge.net/swig/swig-4.3.0.tar.gz && \
    tar -xvzf swig-4.3.0.tar.gz && \
    cd swig-4.3.0 && \
    ./configure && \
    make && \
    make install && \
    ldconfig && \
    rm -rf /tmp/swig-4.3.0 /tmp/swig-4.3.0.tar.gz

ENV DISPLAY="host.docker.internal:0.0"
