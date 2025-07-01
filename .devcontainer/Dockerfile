FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && 
apt install -y qemu-kvm qemu-system-x86 qemu-utils wget unzip tmux curl sudo && 
apt clean

Add user to kvm group (optional, if needed)

RUN usermod -aG kvm vscode || true

Install ngrok manually

RUN wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-stable-linux-amd64.zip && 
unzip ngrok-stable-linux-amd64.zip && 
mv ngrok /usr/local/bin && 
rm ngrok-stable-linux-amd64.zip

SHELL ["/bin/bash", "-c"]
