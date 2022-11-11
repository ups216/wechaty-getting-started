FROM registry.cn-hangzhou.aliyuncs.com/smartide/smartide-node-v2-vscode-vmlc:latest
LABEL maintainer="Lei Xu <leixu@leansoftx.com>"

RUN cd /tmp \
  && wget https://github.com/yudai/gotty/releases/download/v2.0.0-alpha.3/gotty_2.0.0-alpha.3_linux_amd64.tar.gz \
  && tar zxvf ./gotty*.tar.gz \
  && rm -f gotty*.tar.gz \
  && mv gotty* /usr/local/bin

RUN apt-get update && \
    apt-get -y install --no-install-recommends libgconf-2-4 libatk1.0-0 libatk-bridge2.0-0 libgdk-pixbuf2.0-0 libgtk-3-0 libgbm-dev libnss3-dev libxss-dev && \
    apt-get clean && \
    apt-get autoremove -y && \
    rm -rf /tmp/* /var/lib/apt/lists/* /var/tmp/*
