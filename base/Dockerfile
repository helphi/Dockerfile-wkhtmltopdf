FROM ubuntu:bionic-20181018

ENV LANG=C.UTF-8 TZ=CST-8

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y wget xorg --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*


