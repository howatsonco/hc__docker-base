FROM node:lts-slim

RUN mkdir /app && \
    apt-get update -y --fix-missing && \
    apt-get upgrade -y && \
    apt install -y curl vim zip && \
    apt-get clean

# Add in the different package managers
RUN curl -fsSL https://get.pnpm.io/install.sh | sh - && \
    npm install -g yarn && \
    curl -f https://get.pnpm.io/v6.16.js | node - add --global pnpm

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install

WORKDIR /app/

