FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y cmake pkg-config build-essential autoconf curl libtool unzip flex bison python
RUN apt-get install -y python-dev
RUN sudo apt-get install -y python3.5-dev

RUN pip install --upgrade pip
RUN pip install wheel

RUN git clone https://github.com/ray-project/ray.git
WORKDIR ./ray
RUN pip wheel --wheel-dir=python ray
