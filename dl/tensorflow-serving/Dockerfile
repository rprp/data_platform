# FROM nvidia image
FROM daocloud.io/rprp/cuda-bazel:cuda-bazel-0.4.2
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN CUDNN_DOWNLOAD_SUM=a87cb2df2e5e7cc0a05e266734e679ee1a2fadad6f06af82a76ed81a23b102c8 \
 && curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v5.1/cudnn-8.0-linux-x64-v5.1.tgz -O \
 && echo \"$CUDNN_DOWNLOAD_SUM  cudnn-8.0-linux-x64-v5.1.tgz\" | sha256sum -c --strict - \
 && tar -xzf cudnn-8.0-linux-x64-v5.1.tgz -C /usr/local \
 && rm cudnn-8.0-linux-x64-v5.1.tgz \
 && ldconfig

RUN git clone --recurse-submodules https://github.com/tensorflow/serving \
    && rm -rf serving/.git

RUN cd serving/tensorflow
