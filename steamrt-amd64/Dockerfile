FROM jimbly/steamrt-precise-amd64-base

RUN apt-get update && apt-get install --force-yes -y --no-install-recommends \
  # skipping: ubuntu-minimal pkg-config time gdb
  build-essential \
  steamrt-dev \
  && rm -rf /var/lib/apt/lists/* && \
# Install version matching the latest 32-bit CMake
  wget -q --no-check-certificate https://cmake.org/files/v3.6/cmake-3.6.3-Linux-x86_64.tar.gz && \
  tar xzf ./cmake-3.6.3-Linux-x86_64.tar.gz && \
  cp -r cmake-3.6.3-Linux-x86_64/bin cmake-3.6.3-Linux-x86_64/share /usr/local/ && \
  rm -r cmake*
