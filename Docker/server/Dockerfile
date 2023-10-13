FROM ubuntu:20.04
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update
RUN apt install build-essential checkinstall zlib1g-dev -y
RUN yes | apt-get install git
RUN yes | apt-get -y install cmake
RUN yes | apt-get install libssl-dev
RUN yes | git clone https://github.com/Alibaba-Gemini-Lab/OpenCheetah.git
RUN yes | apt install libomp-dev
WORKDIR /OpenCheetah
RUN bash scripts/build-deps.sh; exit 0
RUN bash scripts/build-deps.sh
RUN bash scripts/build.sh
EXPOSE 12345

