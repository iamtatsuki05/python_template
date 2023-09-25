FROM python:3.9-slim

WORKDIR /main

RUN apt-get update && apt-get install -y\
  vim neovim nano \
  git git-lfs \
  zip unzip \
  curl make build-essential xz-utils file tree \
  sudo \
  && pip install --upgrade pip \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*


# install python packages
COPY requirements.txt /main
RUN pip install -r requirements.txt
