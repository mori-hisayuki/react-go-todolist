FROM golang:latest

RUN go install github.com/air-verse/air@latest

# node22.7.0 install
RUN set -x \
    && apt-get -y update \
    && curl -fsSL https://deb.nodesource.com/setup_22.x | bash - \
    && apt-get install -y --no-install-recommends \
    nodejs=22.7.0-1nodesource1  \
    && apt-get clean && rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*

# pnpm install
RUN npm install -g pnpm

WORKDIR /develop
