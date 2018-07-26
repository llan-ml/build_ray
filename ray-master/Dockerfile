FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y cmake pkg-config build-essential autoconf curl libtool unzip flex bison python
RUN apt-get install -y python3.5 python3.5-dev python3-pip

RUN pip3 install --upgrade pip3
RUN pip3 install wheel

RUN git clone https://github.com/ray-project/ray.git
WORKDIR ./ray/python
RUN python3.5 setup.py bdist_wheel
