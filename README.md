# docker-exemplo-basico
Repositório exemplo para uso didático. Aprendizado de Docker

## O que irá encontrar no repositório?
Neste repositório, temos exemplos básicos de execução de contêineres utilzando Docker.

## Como configurar o seu ambiente

### Pré Requisito
Navegue até o diretório `exercícios`, abra o README.md contido na pasta e siga o passo a passo da instalação do Docker.

### Estrutura do repositório
```
|__.github                          # Pasta com os arquivos de CI/CD para o GitHub Actions
|__exercicios                       # Exercícios 
|  |__1-... 
|  |  |__Dockerfile                    # Arquivo principal para execução do Docker
|  |__2-...                          
|__imagens                          # Imagens ilustrativas utilizadas na contrução deste repositório
|__CHANGELOG.md                     # Arquivo de controle de changes do repositório
|__CONTRIBUTING.md                  # Arquivo com diretrizes de contribuição
|__package.json                     # Arquivo necessário para geração de versionamento automático
|__README.md                        # Você está lendo esse arquivo
|__.versionrc                       # Arquivo necessário para configuração de versionamento
```

### Como executar os exercícios

- Navegue até o diretório do exercício desejado e construa a imagem utilizando o comando `docker build -t hello-docker .`

- Depois execute o contêiner utilizando o comando `docker run hello-docker`


## Contribuindo
Contribuições são bem-vindas! Por favor, leia o arquivo [CONTRIBUTING.md](CONTRIBUTING.md) para mais detalhes.

### Controle de versão
Para control de versão automático usamos a lib [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version)