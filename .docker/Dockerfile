FROM python:3.11
RUN update-ca-certificates --fresh
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y sshpass rsync \
    qemu-kvm bridge-utils libguestfs-tools vagrant-libvirt
ARG ANSIBLE_VERSION
RUN pip install --upgrade pip
ADD requirements.txt /requirements.txt
RUN pip install -r /requirements.txt
WORKDIR /etc/ansible
