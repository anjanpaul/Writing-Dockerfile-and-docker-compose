ARG IMAGE_NAME=python
ARG TAG=latest
FROM ${IMAGE_NAME}:${TAG}


ARG ENVCONSUL_VERSION=0.12.0
ARG ARCH=linux_amd64
RUN apt update && apt install -y \
    python3-pip \
    unzip \
    wget \
    && wget -O /tmpenvconsul.zip https://releases.hashicorp.com/envconsul/${ENVCONSUL_VERSION}}/envconsul_${ENVCONSUL_VERSION}}_${ARCH}}.zip \
    && unzip /tmp/envconsul.zip \
    && rm -fr /tmp/envconsul.zip \
    && mv envconsul /usr/local/bin \
    && chmod +x /usr/local/bin/envconsul \
    && apt remove --purge -y unzip wget
CMD ["envconsul", "-h"] 


# docker build --build-arg IMAGE_NAME=ubuntu -t envconsul:0.0.1 .

# export TEST="hello"
# python3 
# import os
# os.environ["TEST"]