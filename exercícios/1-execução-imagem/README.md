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
