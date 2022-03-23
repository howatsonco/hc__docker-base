FROM node:lts-slim

RUN mkdir /app && \
    apt-get update -y --fix-missing && \
    apt-get upgrade -y && \
    apt install -y curl vim zip && \
    apt-get clean

RUN curl -fsSL https://get.pnpm.io/install.sh | sh -
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install

WORKDIR /app/

EXPOSE 80 443 9000 3000 6006
