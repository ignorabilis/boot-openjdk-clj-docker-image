FROM openjdk:8-alpine
MAINTAINER Irina Yaroslavova Stefanova <irina.yaroslavova@ignorabilis.com>

ENV BOOT_HOME /.boot
ENV BOOT_AS_ROOT yes
ENV BOOT_LOCAL_REPO /m2
ENV BOOT_JVM_OPTIONS=-Xmx2g

RUN apk add --update tar gnupg bash openssl && rm -rf /var/cache/apk/* \
    && wget -O /usr/bin/boot https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh \
    && chmod +x /usr/bin/boot \
    && /usr/bin/boot web -s doesnt/exist repl -e '(System/exit 0)' && rm -rf target

ENTRYPOINT ["/usr/bin/boot"]
