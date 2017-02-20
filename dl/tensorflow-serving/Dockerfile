# FROM nvidia image
FROM daocloud.io/rprp/cuda-bazel:cuda-bazel-0.4.4
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN apt-get update && apt-get install -y \
        build-essential \
        libcurl3-dev \
        git \
        libfreetype6-dev \
        libpng12-dev \
        libzmq3-dev \
        pkg-config \
        python-dev \
        python-numpy \
        python-pip \
        swig \
        zip \
        zlib1g-dev \
    && apt-get clean all \
    && git clone --recurse-submodules https://github.com/tensorflow/serving

RUN cd serving/tensorflow
