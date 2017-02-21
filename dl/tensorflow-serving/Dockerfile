# FROM nvidia image
FROM daocloud.io/rprp/cuda-bazel:cuda-bazel-0.4.2
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN git clone --recurse-submodules https://github.com/tensorflow/serving \
    && rm -rf serving/.git

ADD conf.data /serving/tensorflow/conf.data

RUN cd serving/tensorflow && ./configure < conf.data 
RUN cd /serving && bazel build tensorflow_serving/...
