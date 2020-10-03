FROM ubuntu:20.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y build-essential cmake gcc git libboost-all-dev
RUN git clone https://github.com/mskashi/kv.git /usr/local/include/
RUN git clone https://github.com/mskashi/kv.git /usr/local/kv
WORKDIR /usr/local/kv
CMD c++ -I.. -I/usr/local/include /usr/local/kv/test/test-interval.cc && \
    ./a.out
