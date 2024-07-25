# Usar a imagem base do Ubuntu
FROM ubuntu:latest

# Atualiza a lista de pacotes e instala o Nginx
RUN apt-get update && apt-get install -y nginx

# Copia o arquivo de configuração do Nginx
COPY nginx.conf /etc/nginx/sites-available/nginx.conf 

# Exporta a porta 80
EXPOSE 80

# Define o comando para iniciar o Nginx
CMD ["nginx", "-g", "daemon off;"]


# 1. Navegue até o diretório do projeto e construa a imagem utilizando o comando `docker build -t hello-nginx . .`

# 2. Agora que a imagem foi construída, você pode executar o contêiner do Nginx com o seguinte comando: `docker run -d -p 80:80 hello-nginx`

# 3. Abra um navegador web e acesse http://localhost. Se tudo estiver correto, você verá a página padrão do Nginx.

