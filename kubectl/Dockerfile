FROM docker:19.03

ENV PATH="/root/google-cloud-sdk/bin:${PATH}"

RUN apk add --no-cache \
    jq \
    unzip \
    curl \
    python3 \
    which \
    bash \
    && curl -sSL https://sdk.cloud.google.com | bash \
    && curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/kubectl \
    && rm -rf /var/cache/apk/*
