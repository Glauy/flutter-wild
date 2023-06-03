FROM dart


# 设置工作目录
WORKDIR /workspace/flutter_first

USER root
# 安装Flutter的依赖项
RUN apt-get update
RUN apt-get install -y curl git unzip xz-utils zip libglu1-mesa
RUN apt-get clean
# 添加用户
RUN useradd -ms /bin/bash flutter
USER flutter
# 下载和安装Flutter
RUN git clone https://github.com/flutter/flutter.git -b stable --depth 1 ~/flutter \
    && echo 'export PATH="$PATH:/home/glauy/flutter/bin"' >> ~/.bashrc

RUN flutter doctor