FROM ubuntu:latest

ARG PASSWORD_ENV
ARG ADDR_ENV

ENV PASSWORD_ENV $PASSWORD_ENV
ENV ADDR_ENV $ADDR_ENV

RUN mkdir /opt/merlin
WORKDIR /opt/merlin

RUN apt update
RUN apt install -y wget p7zip-full

RUN wget https://github.com/Ne0nd0g/merlin/releases/latest/download/merlinServer-Linux-x64.7z
RUN 7z x merlinServer-Linux-x64.7z -pmerlin

CMD ./merlinServer-Linux-x64 -password ${PASSWORD_ENV} -addr ${ADDR_ENV}