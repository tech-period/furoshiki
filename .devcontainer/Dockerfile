FROM node:18.10-slim

WORKDIR /home/node/furoshiki

# Install basic development tools
RUN apt update && apt install -y less man-db sudo
RUN echo y | apt-get install git

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
