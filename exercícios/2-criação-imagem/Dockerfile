FROM alpine:latest

# Instalando as novas dependências curl e bash
RUN apk add --no-cache python3 py3-pip curl bash

COPY hello_docker.py /hello_docker.py

CMD ["python3", "/hello_docker.py"]

# 1. Navegue até o diretório do projeto e construa a imagem utilizando o comando `docker build -t hello-docker .`

# 2. Depois execute o contêiner utilizando o comando `docker run hello-docker /bin/bash` para acessar o contêiner.

# 3. Execute os comandos curl `--version` e `bash --version` para verificar se os pacotes estão instalados corretamente.