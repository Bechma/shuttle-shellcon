FROM mcr.microsoft.com/devcontainers/rust:latest

# Install additional packages
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install curl wget htop \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Shuttle CLI
RUN cargo install cargo-shuttle

# Set up environment variables
ENV RUST_BACKTRACE=1

WORKDIR /workspaces
