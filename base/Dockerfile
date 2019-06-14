FROM ubuntu:16.04

ENV NODE_VERSION 8.x
ENV YARN_VERSION 1.12.3

RUN apt-get update \
    && apt-get install -y build-essential git gcc curl wget tar vim make g++ python-software-properties python-pip \
    && curl -sL https://deb.nodesource.com/setup_${NODE_VERSION} | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/* \
    && npm install -g yarn@${YARN_VERSION} \
    && pip install --upgrade pip

RUN pip --no-cache-dir install awscli --upgrade

CMD ["/bin/bash"]
