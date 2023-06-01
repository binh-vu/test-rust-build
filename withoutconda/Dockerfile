FROM quay.io/pypa/manylinux2014_x86_64:latest

RUN yum update -y
RUN yum install -y llvm-toolset-7
RUN curl --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y --profile minimal --default-toolchain stable
RUN /opt/python/cp311-cp311/bin/pip install maturin
RUN mkdir /tmp/deleteme \
    && cd /tmp/deleteme \
    && /root/.cargo/bin/cargo init \
    && /root/.cargo/bin/cargo add serde \
    && rm -rf /tmp/deleteme

ENV PATH="/opt/python/cp311-cp311/bin/:$PATH"