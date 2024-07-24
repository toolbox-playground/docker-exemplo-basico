# Instalação do Docker no Windows

## Pré-requisitos

### Antes de começar a instalação, certifique de ter no mínimo:

- **Sistema Operacional:** Windows 10 ou superior.
  
- **Processador:** 64-bit
  
- **Memória:** 4 GB de RAM

### 1. Baixar o Docker Desktop

1. Abra seu navegador web e vá para a página oficial de download do Docker: [Docker Desktop](https://www.docker.com/products/docker-desktop).
   
2. Clique em "**Download for Windows**".

### 2. Executar o Instalador

1. Após o download, execute o arquivo `Docker Desktop Installer.exe`.

2. Siga as instruções do instalador. Quando a instalação for concluida, clique em "**Close**".

### 3. Finalizar a Instalação do Docker Desktop

1. Após a instalação do Docker Desktop, procure por Docker e selecione "**Docker Desktop**" nos resultados.
   

    ![Docker Search](../imagens/docker-app-search.png)


2. Durante a primeira execução, será solicitado para fazer login ou criar uma conta Docker.


### 4. Verificação da Instalação

1. Abra o terminal PowerShell (Terminal).
   
2. Execute o comando para verificar a versão do Docker instalada:
   
    ```bash
    docker --version
    ```

   Você deve ver uma saída semelhante a:
    ```
    Docker version 20.10.8, build 3967b7d
    ```


### 5. Testar o Docker

1. No terminal, execute o comando para rodar um container de teste:
   
    ```bash
    docker run hello-world
    ```

   Este comando faz o download de uma imagem de teste do Docker Hub e executa um container que imprime uma mensagem de "**Hello from Docker!**".

   ![Hello Docker](../imagens/hello-docker.png)

### 6. Verificação do Docker Engine

1. Execute o comando abaixo para listar todos os containers ativos. Se não houver containers rodando, retornará uma lista vazia:
   

    ```bash
    docker ps
    ```

2. Execute o comando abaixo para listar todos os contêineres, incluindo os que estão parados:
    ```bash
    docker ps -a
    ```

# Docker Hub

### O Docker Hub é um repositório de imagens Docker, onde é possível encontrar e baixar imagens de container que foram criadas e compartilhadas por outras pessoas.


### 1. Procurarando Imagens

#### Acesse [hub.docker.com](hub.docker.com) e use a barra de pesquisa para encontrar a imagem desejada.

![Hello Docker](../imagens/docker-hub.png)

### 2. Baixando Imagens

#### Para baixar uma imagem, utilize o comando:

```
docker pull <nome-da-imagem>
```

#### Por exemplo, para baixar a imagem ubuntu:

```
docker pull ubuntu
```

# Dockerfile

### Um Dockerfile é um arquivo que contém instruções que o Docker lê e executar uma ação, como instalar pacotes, copiar arquivos, definir comandos a serem executados no contêiner, entre outros, afim de criar uma imagem específica.

## Criando um Dockerfile Simples

#### Vamos criar um Dockerfile básico para construir uma imagem baseada no Alpine Linux.

```dockerfile
FROM alpine:latest

RUN apk update && apk add bash

CMD ["echo", "Hello World from Docker!"]
```

### Explicação dos Comandos
1. FROM alpine

    Indica a imagem base que será utilizada. Neste caso, usaremos a última versão (latest) da imagem alpine.

2. RUN apk update && apk add bash

    Executa comandos dentro do contêiner durante a construção da imagem. Aqui, iremos atualizar os pacotes do Alpine (apk update) e instalar o pacote bash (apk add bash).

3. CMD ["echo", "Hello World from Docker!"]

    Especifica o comando que será utilizado quando o contêiner é iniciado. Neste exemplo, estamos utilizando o comando echo para imprimir a mensagem "Hello World from Docker!".

### Construindo a Imagem Docker

1. Crie um arquivo chamado `Dockerfile` e copie o conteúdo acima para dentro dele.

2. No terminal, navegue até o diretório onde o Dockerfile está localizado.

3. Execute o comando a seguir para construir a imagem.

```
docker build -t minha-primeira-imagem
```

### Agora vamos testar a imagem construída

1. Execute o seguinte comando:

```
docker run minha-primeira-imagem
```

2. A saída esperada deve ser:

```
Hello World from Docker!
```