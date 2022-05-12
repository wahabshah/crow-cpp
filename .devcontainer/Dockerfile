# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.202.5/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version (use bullseye or stretch on local arm64/Apple Silicon): bullseye, buster, stretch
ARG VARIANT="bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

#** [Optional] Uncomment this section to install additional packages. **
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends build-essential libboost-all-dev cmake netcat gdb \ 
                                                  clang  clangd  clang-format  clang-tidy  lld

RUN git clone -b v1.0 https://github.com/CrowCpp/Crow.git /tmp/crow-src  &&  \
    cd /tmp/crow-src                                                     &&  \
    mkdir build                                                          &&  \
    cd build                                                             &&  \
    cmake .. -DCROW_BUILD_EXAMPLES=OFF -DCROW_BUILD_TESTS=OFF            &&  \
    make install
