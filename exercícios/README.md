# Docker Hub
O Docker Hub é um repositório de imagens Docker, onde é possível encontrar e baixar imagens de container que foram criadas e compartilhadas por outras pessoas.

## 1. Procurarando Imagens

Acesse [Docke Hub](hub.docker.com) e use a barra de pesquisa para encontrar a imagem desejada.

## 2. Baixando Imagens

Para baixar uma imagem, utilize o comando:

```docker pull <nome-da-imagem>```

Por exemplo, para baixar a imagem ubuntu:

```docker pull ubuntu```

## Dockerfile

Um Dockerfile é um arquivo que contém instruções que o Docker lê e executar uma ação, como instalar pacotes, copiar arquivos, definir comandos a serem executados no contêiner, entre outros, afim de criar uma imagem específica.

## Criando um Dockerfile Simples

Vamos criar um Dockerfile básico para construir uma imagem baseada no Alpine Linux.

```dockerfile
FROM alpine:latest

RUN apk update && apk add bash

CMD ["echo", "Hello World from Docker!"]