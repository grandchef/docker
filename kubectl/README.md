# GrandChef - Docker Image for Build
Imagem docker para construir container.

## Build

Criar imagem
```sh
docker build -t grandchef/docker:23.0.1-kubectl kubectl
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/docker:23.0.1-kubectl /bin/bash
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/docker:23.0.1-kubectl
```
