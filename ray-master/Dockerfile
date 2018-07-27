FROM quay.io/xhochy/arrow_manylinux1_x86_64_base:latest

WORKDIR /
RUN git clone https://github.com/ray-project/ray.git
COPY ./build-wheel-manylinux1.sh /ray/python

WORKDIR /ray
RUN /ray/python/build-wheel-manylinux1.sh
