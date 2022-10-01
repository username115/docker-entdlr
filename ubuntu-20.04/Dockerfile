FROM ubuntu:20.04

RUN apt-get update

RUN apt-get install tzdata

RUN dpkg-reconfigure -f noninteractive tzdata

RUN apt-get install -y g++ git cmake

RUN git clone https://github.com/tstraus/entdlr

WORKDIR entdlr

RUN git checkout b306a077d2f68bb4f2c0e74b7dbcb82e99ec24df

RUN cmake .
RUN cmake --build . --config Release --target install
