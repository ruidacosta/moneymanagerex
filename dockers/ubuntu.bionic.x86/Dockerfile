FROM ubuntu:bionic
MAINTAINER developers@moneymanagerex.org
RUN dpkg --add-architecture i386 && apt-get update && \
    apt-get install -y --no-install-recommends \
      cmake build-essential g++-multilib gettext git pkg-config lsb-release \
      libwxgtk-webview3.0-gtk3-dev:i386 liblua5.3-dev:i386 libcurl4-openssl-dev:i386\
      automake libtool ccache && \
    apt-get clean

ENV MMEX_INST_CMD apt install -yqV ./mmex_*.deb
