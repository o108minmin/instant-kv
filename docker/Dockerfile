FROM ubuntu:20.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y build-essential cmake gcc git libboost-all-dev
RUN git clone https://github.com/mskashi/kv.git /usr/local/include/
WORKDIR /usr/local/include/kv
ARG COMMIT=master
RUN git checkout $COMMIT
CMD c++ -I.. -I/usr/local/include /app/main.cc && \
    ./a.out
