FROM docker:23.0.1

ENV PATH="/root/google-cloud-sdk/bin:${PATH}"

RUN apk add --no-cache \
    jq \
    unzip \
    curl \
    python3 \
    which \
    bash \
    gettext \
    && curl -sSL https://sdk.cloud.google.com | bash \
    && curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl \
    && gcloud components install --quiet gke-gcloud-auth-plugin \
    && mv ./kubectl /usr/local/bin/kubectl \
    && rm -rf /var/cache/apk/*
