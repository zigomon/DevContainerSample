FROM mcr.microsoft.com/devcontainers/go:1-1.24-bookworm

# zshと依存関係をインストール
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends zsh curl git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY .zshrc /home/vscode/.zshrc
RUN chown vscode:vscode /home/vscode/.zshrc
