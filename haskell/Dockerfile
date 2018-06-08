FROM build-env

RUN apt-get install -y curl
RUN curl -sSL https://get.haskellstack.org/ | sh
RUN stack update
RUN stack setup
# popuate index cache
RUN stack ghc || true

VOLUME /root/.stack/
WORKDIR /src
