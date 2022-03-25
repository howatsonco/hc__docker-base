FROM node:lts-slim

RUN mkdir /app && \
    apt-get update -y --fix-missing && \
    apt-get upgrade -y && \
    apt install -y curl vim zip && \
    apt-get clean

# Add in the different package managers
RUN npm install -g yarn pnpm

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install

WORKDIR /app/

