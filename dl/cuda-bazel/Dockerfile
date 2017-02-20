# FROM nvidia image
FROM nvidia/cuda
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN add-apt-repository ppa:webupd8team/java \
 && apt-get update \
 && apt-get install oracle-java8-installer \
 && echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | tee /etc/apt/sources.list.d/bazel.list \
 && curl https://bazel.build/bazel-release.pub.gpg | sudo apt-key add - \
 && apt-get install bazel \
 && sudo apt-get upgrade bazel
