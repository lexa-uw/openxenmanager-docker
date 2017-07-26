FROM debian:stable

RUN apt-get update

RUN apt-get -y install python-gtk2 glade python-gtk-vnc python-glade2 \
    python-configobj curl zip

RUN curl https://codeload.github.com/OpenXenManager/openxenmanager/zip/master \
    -o /tmp/openxenmanager.zip -s
RUN mkdir -p /opt/openxenmanager && mkdir -p ~/.local/share
RUN unzip /tmp/openxenmanager.zip -d /opt/openxenmanager

WORKDIR /opt/openxenmanager/openxenmanager-master
ENTRYPOINT ["./openxenmanager"]
