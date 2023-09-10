FROM ubuntu:22.04

WORKDIR /tmp

# 共通利用のパッケージのインストール
RUN apt update && \
    apt upgrade -y && \
    apt install -y less sudo curl unzip git

ENV SHELL bash
ARG USERNAME=node
RUN useradd -m $USERNAME && \
    echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME

# terraformのインストール（バイナリを落としてきてパスの通っているところに解凍する方法）
ENV TF_VERSION=1.5.0
RUN curl "https://releases.hashicorp.com/terraform/${TF_VERSION}/terraform_${TF_VERSION}_linux_amd64.zip" -o "terraform.zip"
RUN sudo unzip -d /usr/local/bin/ terraform.zip
RUN rm terraform.zip

RUN echo "alias tf='terraform'" >> /home/node/.bashrc