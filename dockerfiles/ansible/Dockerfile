FROM archlinux:latest
LABEL maintainer "Peter Kay <contact@kaypeter.com>"

RUN pacman -Syu --noconfirm ansible && yes | pacman -Scc && rm -fr /var/lib/pacman/sync/*

ENTRYPOINT ["ansible"]
