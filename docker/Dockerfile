## Dockerfile

FROM python:3.10.7

ARG PGID=1000
ARG PUID=1000

RUN apt-get update

RUN groupadd -g ${PGID} webui
RUN useradd -l -u ${PUID} -g webui -m webui
RUN usermod -p "*" webui -s /bin/bash

USER webui

RUN mkdir ~/app

WORKDIR /home/webui/app

COPY . ./

CMD ./webui.sh