FROM ubuntu:bionic-20181018

ENV LANG=C.UTF-8 TZ=CST-8

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y wget xorg --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN wget --no-check-certificate https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz -O wkhtmltox.tar.xz &&\
    tar xvf wkhtmltox.tar.xz &&\
    rm -rf wkhtmltox.tar.xz &&\
    mv wkhtmltox /wkhtmltox

ENV PATH=/wkhtmltox/bin:$PATH

CMD [ "wkhtmltopdf", "--help" ]


