FROM ubuntu:18.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y build-essential libtool autotools-dev automake \ 
    pkg-config bsdmainutils python3 libssl-dev libevent-dev libboost-system-dev \ 
    libboost-filesystem-dev libboost-chrono-dev libboost-test-dev \ 
    libboost-thread-dev software-properties-common 
RUN add-apt-repository ppa:bitcoin/bitcoin
RUN apt-get install -y libdb4.8-dev libdb4.8++-dev git
RUN git clone https://github.com/whiveio/whive.git
RUN cd whive && \
    ./autogen.sh && \ 
    ./configure && \
    make && \ 
    make install

WORKDIR         /whive

