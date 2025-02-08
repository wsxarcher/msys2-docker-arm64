FROM debian:bookworm AS build

# Install WINE
RUN apt update && \
    DEBIAN_FRONTEND="noninteractive" apt install -y wget && \
    wget https://github.com/wsxarcher/hangover-msys2/releases/download/hangover-10.0-msys2/hangover_10.0-msys2_debian12_bookworm_arm64.tar -O hangover.tar && \
    tar -xf *.tar && \
    DEBIAN_FRONTEND="noninteractive" apt install -y ./*.deb && \
    rm -rf *.tar *.deb