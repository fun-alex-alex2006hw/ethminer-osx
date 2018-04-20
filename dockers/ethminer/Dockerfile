FROM nvidia/cuda:8.0-devel-ubuntu16.04

MAINTAINER Anthony Tatowicz

WORKDIR /

# Package and dependency setup
RUN apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get install -y ethereum ethminer

COPY docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT [ "/docker-entrypoint.sh" ]
