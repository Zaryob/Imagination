FROM alpine:latest as stage1

RUN apk add --no-cache gcc musl-dev curl
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- --default-toolchain none -y

USER root
ARG USER=root
ENV PATH="/${USER}/.cargo/bin:${PATH}"
ENV CARGO_HOME="/${USER}/.cargo"
ENV RUSTUP_HOME="/${USER}/.rustup"

RUN rustup toolchain install nightly --allow-downgrade --profile minimal --component clippy
RUN apk del --no-cache curl

RUN rm -f {/sbin/apk,/etc/apk,/lib/apk,/usr/share/apk,/var/lib/apk}

FROM scratch
LABEL maintainer="zaryob.dev@gmail.com"

USER root
ARG USER=root
ENV PATH="/${USER}/.cargo/bin:${PATH}"
ENV CARGO_HOME="/${USER}/.cargo"
ENV RUSTUP_HOME="/${USER}/.rustup"

COPY --from=stage1 / /
ENTRYPOINT ["/bin/sh"]
