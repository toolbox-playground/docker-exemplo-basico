# Utiliza a imagem base do Alpine Linux
FROM alpine:latest

# Atualiza o apk e instala o Python
RUN apk add --no-cache python3 py3-pip

# Copia o script Python para o contêiner
COPY hello_docker.py /hello_docker.py

# Define o comando padrão para a execução do script Python
CMD ["python3", "/hello_docker.py"]

# Navegue até o diretório do projeto e construa a imagem utilizando o comando `docker build -t hello-docker .`

# Depois execute o contêiner utilizando o comando `docker run hello-docker`