# GrandChef - Docker Image for Build
Imagem docker para construir container.

## Build

Criar imagem
```sh
docker build -t grandchef/docker:19.03-kubectrl kubectrl
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/docker:19.03-kubectrl /bin/bash
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/docker:19.03-kubectrl
```
