FROM ubuntu:xenial

LABEL description="Base image for Ethereum (ETH) fullnode"
LABEL maintainer="mike@r3lik.com"
LABEL version="0.1" 

RUN apt-get update && \
    apt-get -y -qq upgrade && \
    apt-get -y -qq install software-properties-common && \
    add-apt-repository ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get -y -qq install geth solc && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 8545
EXPOSE 30303

VOLUME /root

ENTRYPOINT ["geth"]

# allows external calls 
CMD ["--rpc", "--rpcaddr '0.0.0.0'"]
