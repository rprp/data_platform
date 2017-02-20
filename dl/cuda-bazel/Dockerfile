# FROM nvidia image
FROM nvidia/cuda
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN apt-get update \
 && apt-get -y install python-software-properties \
 && apt-get -y install software-properties-common \
 && add-apt-repository -y ppa:webupd8team/java \
 && apt-get -y install oracle-java8-installer \
 && echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | tee /etc/apt/sources.list.d/bazel.list \
 && curl https://bazel.build/bazel-release.pub.gpg | apt-key add - \
 && apt-get -y install bazel \
 && sudo apt-get upgrade bazel
