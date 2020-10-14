FROM archlinux:latest
LABEL maintainer "Peter Kay <contact@kaypeter.com>"

RUN pacman -Syu --needed --noconfirm \
  base-devel \
  sudo \
  git \
  terraform \
  helm \
  vault

ARG user=makepkg
RUN useradd -m $user \
  && echo "$user ALL=(ALL:ALL) NOPASSWD:ALL" > /etc/sudoers.d/$user
USER $user
WORKDIR /home/$user

RUN git clone https://aur.archlinux.org/yay.git \
  && cd yay \
  && makepkg -sri --needed --noconfirm \
  && yay -S --noconfirm --answerdiff=None kubectl-bin \
  && cd \
  && rm -rf .cache yay
