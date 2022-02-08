FROM gradle:jdk8

RUN apt-get update

RUN apt-get install tzdata

RUN dpkg-reconfigure -f noninteractive tzdata

RUN apt-get install -y g++ git cmake

RUN git clone https://github.com/tstraus/entdlr

WORKDIR entdlr

RUN cmake .
RUN cmake --build . --config Release --target install
