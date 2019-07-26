FROM ubuntu:latest
LABEL maintainer="Henrik Sommerfeld <henrik@sommerfeld.nu>"

RUN apt-get update && apt-get install -y sudo curl git-core gnupg linuxbrew-wrapper locales nodejs zsh wget nano nodejs npm fonts-powerline && npm install -g gatsby-cli && locale-gen en_US.UTF-8 && adduser --quiet --disabled-password --shell /bin/zsh --home /home/devuser --gecos "User" devuser && echo "devuser:p@ssword1" | chpasswd && usermod -aG sudo devuser
USER devuser
ENV TERM xterm
ENV ZSH_THEME agnoster
CMD ["zsh"]