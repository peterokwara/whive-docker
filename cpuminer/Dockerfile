FROM ubuntu:18.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y build-essential libcurl4-openssl-dev git make autotools-dev automake
RUN git clone https://github.com/cryptozeny/cpuminer-mc-yespower.git
RUN cd cpuminer-mc-yespower && \
    ./autogen.sh && \
    ./configure CFLAGS="-O3" && \
    make

WORKDIR         /cpuminer-mc-yespower
