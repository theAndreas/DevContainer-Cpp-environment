FROM mcr.microsoft.com/devcontainers/cpp:1-ubuntu-24.04

# Install additional tools
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
        clang \
        clangd \
        cmake \
        clang-tidy \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*
