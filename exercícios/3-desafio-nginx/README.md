1. Navegue até o diretório do projeto e construa a imagem utilizando o comando `docker build -t hello-nginx . .`

2. Agora que a imagem foi construída, você pode executar o contêiner do Nginx com o seguinte comando: `docker run -d -p 80:80 hello-nginx`

3. Abra um navegador web e acesse http://localhost. Se tudo estiver correto, você verá a página padrão do Nginx.
