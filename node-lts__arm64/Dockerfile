FROM node:lts-slim

RUN mkdir /app && \
    apt-get update -y --fix-missing && \
    apt-get upgrade -y && \
    apt install -y curl vim zip less && \
    apt-get clean

# Add in pnpm
RUN npm install -g pnpm

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" && \
  unzip awscliv2.zip && \
  ./aws/install && \
  rm -rf ./aws && \
  rm awscliv2.zip

WORKDIR /app/

