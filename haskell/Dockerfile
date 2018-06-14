FROM debian:9.4

RUN apt-get update
RUN apt-get install -y build-essential curl
RUN curl -sSL https://get.haskellstack.org/ | sh
RUN stack update
RUN stack setup
# popuate index cache
RUN stack ghc || true

VOLUME /root/.stack/
VOLUME /workspace/

WORKDIR /workspace

