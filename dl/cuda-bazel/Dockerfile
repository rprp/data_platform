# FROM nvidia image
FROM nvidia/cuda
MAINTAINER renpeng <renpeng@autohome.com.cn>

RUN apt-get update \
 && apt-get -y install curl \
 && apt-get -y install python-software-properties \
 && apt-get -y install software-properties-common \
 && add-apt-repository -y ppa:webupd8team/java \
 && apt-get update -y \
 && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886 \
 && echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
 && apt-get -y install oracle-java8-installer \
 && apt-get install -y oracle-java8-unlimited-jce-policy \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* \
 && rm -rf /var/cache/oracle-jdk8-installer \
 && echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | tee /etc/apt/sources.list.d/bazel.list \
 && curl https://bazel.build/bazel-release.pub.gpg | apt-key add - \
 && apt-get update -y \
 && apt-get -y install bazel \
 && apt-get -y upgrade bazel

ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
