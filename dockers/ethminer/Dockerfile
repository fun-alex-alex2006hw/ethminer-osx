FROM nvidia/cuda:8.0-devel-ubuntu16.04

MAINTAINER Anthony Tatowicz

WORKDIR /

# Package and dependency setup
RUN apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get install -y ethereum ethminer

ENTRYPOINT ["/usr/bin/ethminer", "-F", "http://eth-us-west1.nanopool.org:8888/0x49Ed989fF5D7B58D81ea76FDC043a9990778e17D/data_cpu_worker01/eth-uswest1-nanopool@alex2006hw.com"]
