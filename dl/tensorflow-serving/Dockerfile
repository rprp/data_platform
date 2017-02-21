# FROM nvidia image
FROM daocloud.io/rprp/cuda-bazel:cuda-bazel-0.4.4
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN git clone --recurse-submodules https://github.com/tensorflow/serving \
    && rm -rf serving/.git

RUN cd serving/tensorflow
