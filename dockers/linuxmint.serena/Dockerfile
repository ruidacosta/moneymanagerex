FROM vcatechnology/linux-mint:18.1
MAINTAINER developers@moneymanagerex.org
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      cmake build-essential gettext git lsb-release \
      libwxgtk-webview3.0-dev liblua5.3-dev libcurl4-openssl-dev \
      automake libtool ccache && \
    apt-get clean

ENV MMEX_INST_CMD apt install -yqV ./mmex_*.deb
