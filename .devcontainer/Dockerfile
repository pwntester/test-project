# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.203.0/containers/python-3/.devcontainer/base.Dockerfile

# [Choice] Python version (use -bullseye variants on local arm64/Apple Silicon): 3, 3.10, 3.9, 3.8, 3.7, 3.6, 3-bullseye, 3.10-bullseye, 3.9-bullseye, 3.8-bullseye, 3.7-bullseye, 3.6-bullseye, 3-buster, 3.10-buster, 3.9-buster, 3.8-buster, 3.7-buster, 3.6-buster
ARG VARIANT="3.7"
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${VARIANT}

# [Choice] Node.js version: none, lts/*, 16, 14, 12, 10
ARG NODE_VERSION="none"
RUN if [ "${NODE_VERSION}" != "none" ]; then su vscode -c "umask 0002 && . /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"; fi

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends fuse
#RUN curl -OL https://github.com/github/codeql-cli-binaries/releases/download/v2.8.0/codeql-linux64.zip && \
RUN curl -L -s https://api.github.com/repos/github/codeql-cli-binaries/releases/latest | jq -r '.assets[] | select(.content_type == "application/zip" and .name == "codeql-linux64.zip") | {browser_download_url} | .browser_download_url' | wget -qi - && \
    unzip codeql-linux64.zip && \
    mv codeql /opt
ENV PATH="/opt/codeql:${PATH}"
