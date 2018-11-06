FROM quay.io/xhochy/arrow_manylinux1_x86_64_base:latest

WORKDIR /
RUN git clone https://github.com/ray-project/ray.git \
  && git checkout tags/ray-0.5.3 -b 0.5.3 \
  && git branch
COPY ./build-wheel-manylinux1.sh /ray/python
RUN chmod +x /ray/python/build-wheel-manylinux1.sh

WORKDIR /ray
RUN /ray/python/build-wheel-manylinux1.sh
