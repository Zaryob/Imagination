FROM alpine:latest as stage1

RUN apk add --no-cache gcc musl-dev
RUN rm -f {/sbin/apk,/etc/apk,/lib/apk,/usr/share/apk,/var/lib/apk}

FROM scratch
LABEL maintainer="zaryob.dev@gmail.com"

COPY --from=stage1 / /
ENTRYPOINT ["/bin/sh"]
