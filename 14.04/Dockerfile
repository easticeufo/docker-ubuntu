FROM ubuntu:14.04
RUN dpkg --add-architecture i386; \
    apt-get update; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y xz-utils; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y wget; \
    DEBIAN_FRONTEND=noninteractive apt install -y zlib1g; \
    DEBIAN_FRONTEND=noninteractive apt install -y zlib1g-dev; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y device-tree-compiler; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y make; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y git; \
    DEBIAN_FRONTEND=noninteractive apt-get install -y lib32bz2-1.0 lib32z1 lib32ncurses5 lib32ncursesw5 lib32stdc++6 libexpat1-dev:i386; \
    cd /home; \
    wget https://packagecloud.io/github/git-lfs/packages/ubuntu/xenial/git-lfs_2.1.1_amd64.deb/download -O git-lfs_2.1.1_amd64.deb; \
    dpkg -i git-lfs_2.1.1_amd64.deb; \
    wget https://download1483.mediafire.com/3mx0y00nnogg/nu5axdjykyg9d2t/fsl-linaro-toolchain.tar.gz; \
    tar -xzf fsl-linaro-toolchain.tar.gz -C /opt; \
    
    mkdir /opt/03_toolchain; \
    wget https://releases.linaro.org/components/toolchain/binaries/7.3-2018.05/aarch64-linux-gnu/gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu.tar.xz; \
    tar xf gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu.tar.xz -C /opt/03_toolchain; \
    rm gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu.tar.xz; \
    wget https://armkeil.blob.core.windows.net/developer/Files/downloads/gnu-rm/10-2020q4/gcc-arm-none-eabi-10-2020-q4-major-x86_64-linux.tar.bz2; \
    tar -xjf gcc-arm-none-eabi-10-2020-q4-major-x86_64-linux.tar.bz2 -C /opt; \
    rm gcc-arm-none-eabi-10-2020-q4-major-x86_64-linux.tar.bz2;
    
ENV PATH="/opt/03_toolchain/gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu/bin:/opt/fsl-linaro-toolchain/bin:/opt/gcc-arm-none-eabi-10-2020-q4-major/bin:${PATH}"

