## Build an image with the latest GNU Fortran compiler and CMake build system
## This devcontainer is based on the base-debian bookworm (v12)
## https://github.com/devcontainers/images/tree/main/src/base-debian
FROM mcr.microsoft.com/devcontainers/base:bookworm

# Associate this project with the image
LABEL org.opencontainers.image.source="https://github.com/mrxcitement/devc-fortran"

# To build and install GNU Fortran I used commands from their documentation
# https://GNU Fortran.sourceforge.io/faq/index.html#building-GNU Fortran-3-0-release-candidates

# Update system and install GNU Fortran
RUN apt-get update \
    && apt-get -y upgrade \
    && DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
        cmake \
        gfortran \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

