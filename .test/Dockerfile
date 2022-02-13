FROM alpine:3.1

RUN apk update \
    && apk add openssh git \
    && addgroup -S git && adduser -D -S git -G git -s /bin/sh \
    && mkdir -p /home/git/.ssh \
    && chmod 0700 /home/git/.ssh \
    && chown git:git -R /home/git \
    && ssh-keygen -A \
    && sed -i s/^#PasswordAuthentication\ yes/PasswordAuthentication\ no/ /etc/ssh/sshd_config

RUN echo "git:git" | chpasswd
RUN chown -R git:git /home/git

CMD ["/podi/.test/docker-entrypoint.sh"]
