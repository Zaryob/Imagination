FROM alpine:latest as stage1

RUN apk add --no-cache gcc musl-dev curl g++ gmp-dev ncurses-dev libffi-dev make xz tar perl
RUN curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | BOOTSTRAP_HASKELL_NONINTERACTIVE=YES sh

RUN apk del --no-cache curl

RUN rm -f {/sbin/apk,/etc/apk,/lib/apk,/usr/share/apk,/var/lib/apk}

FROM scratch
LABEL maintainer="zaryob.dev@gmail.com"

USER root
ARG USER=root
ENV PATH="${USER}/.cabal/bin:${USER}/.ghcup/bin:${USER}"

COPY --from=stage1 / /
ENTRYPOINT ["/bin/sh"]
