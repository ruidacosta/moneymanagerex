FROM debian:buster-slim
MAINTAINER developers@moneymanagerex.org
ADD --chown=_apt:root https://repos.codelite.org/CodeLite.asc /etc/apt/trusted.gpg.d/
RUN echo 'deb http://repos.codelite.org/wx3.1/debian/ buster devel' \
      >/etc/apt/sources.list.d/CodeLite.list && \
    dpkg --add-architecture i386 && apt-get update && \
    apt-get install -y --no-install-recommends \
      cmake build-essential g++-multilib gettext git pkg-config lsb-release file \
      libwxgtk-webview3.1-dev:i386 \
      libwxsqlite3-3.0-dev:i386 liblua5.3-dev:i386 libcurl4-openssl-dev:i386 \
      automake libtool ccache && \
    apt-get clean

ENV MMEX_INST_CMD apt install -yqV ./mmex_*.deb
