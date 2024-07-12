# This Dockerfile builds an image that can be used to compile Flutter web apps.

ARG FLUTTER_VERSION=3.22.2

FROM ubuntu:latest as flutter
ARG FLUTTER_VERSION

ENV PATH "$PATH:/flutter/bin:/flutter/.pub-cache/bin"

RUN apt-get update -y && apt-get install curl unzip xz-utils git make -y 

RUN curl -LO https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_${FLUTTER_VERSION}-stable.tar.xz && \
    tar -xf flutter_linux_${FLUTTER_VERSION}-stable.tar.xz -C / && \
    rm flutter_linux_${FLUTTER_VERSION}-stable.tar.xz

#RUN git config --global --add safe.directory /flutter

#RUN flutter config --enable-web
