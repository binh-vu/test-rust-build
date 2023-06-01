FROM continuumio/anaconda3:2023.03-1

RUN apt update -y
RUN curl --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y --profile minimal --default-toolchain stable
RUN mkdir /tmp/deleteme \
    && cd /tmp/deleteme \
    && /root/.cargo/bin/cargo init \
    && /root/.cargo/bin/cargo add serde \
    && rm -rf /tmp/deleteme

# uncomment the following line also allow to compile it successfully.
# RUN apt install -y clang-11 build-essential cmake