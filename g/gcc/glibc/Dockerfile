FROM debian:unstable-slim as stage1

RUN echo "deb http://ftp.us.debian.org/debian sid main contrib non-free" > /etc/apt/sources.list
RUN apt update
RUN apt upgrade -y
RUN apt install gcc g++ -y

RUN rm -rf /usr/share/doc /usr/share/man
RUN rm -rf  /usr/share/lintian/profiles/dpkg \
            /usr/share/dpkg \
            /usr/share/bug/dpkg \
            /usr/share/doc/dpkg \
            /usr/lib/dpkg \
            /usr/bin/dpkg \
            /etc/cron.daily/dpkg \
            /etc/dpkg \
            /etc/logrotate.d/dpkg \
            /var/lib/dpkg \
            /usr/share/bug/apt \
            /usr/share/doc/apt \
            /usr/share/bash-completion/completions/apt \
            /usr/lib/dpkg/methods/apt \
            /usr/lib/apt \
            /usr/bin/apt \
            /etc/apt \
            /etc/logrotate.d/apt \
            /var/log/apt \
            /var/cache/apt \
            /var/lib/apt

FROM scratch
LABEL maintainer="zaryob.dev@gmail.com"

COPY --from=stage1 / /
ENTRYPOINT ["/bin/sh"]
