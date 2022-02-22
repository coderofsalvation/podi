FROM alpine:3.9

RUN apk update \
    && echo "http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories \
    && apk update \
    && apk add openssh git socat \
    && addgroup -S git && adduser -D -S git -G git -s /bin/sh \
    && mkdir -p /home/git/.ssh \
    && chmod 0700 /home/git/.ssh \
    && chown git:git -R /home/git \
    && ssh-keygen -A \
    && sed -i s/^#PasswordAuthentication\ yes/PasswordAuthentication\ no/ /etc/ssh/sshd_config

RUN echo "git:git" | chpasswd
RUN chown -R git:git /home/git

CMD ["/podi/.test/docker-entrypoint.sh"]
