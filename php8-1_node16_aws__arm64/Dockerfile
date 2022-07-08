FROM ghcr.io/howatsonco/hc__docker-base:php8-1_node16__arm64

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" && \
  unzip awscliv2.zip && \
  ./aws/install && \
  rm -rf ./aws && \
  rm awscliv2.zip