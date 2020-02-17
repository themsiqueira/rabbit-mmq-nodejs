# RabbitMq worker com nodejs

Um projeto simples para mostrar o uso do rabbitmq com nodejs

# Como configurar o projeto:

### 1. Instale o NodeJS

- _NodeJS:_ https://nodejs.org/en/

### 2. Instale o yarn ou npm

- _yarn:_ https://yarnpkg.com/lang/en/

- _npm:_ https://www.npmjs.com/get-npm

### 3. Instale docker CE ou toolbox  para rodar o banco de dados:

  - _Docker CE:_ https://hub.docker.com/editions/community/docker-ce-desktop-windows

  - _Docker Toolbox:_ https://docs.docker.com/toolbox/toolbox_install_windows/

  > Obs: Os links acima são para instalação no Windows, mas no plataforma você encontrará a documentação para outros SO's.

# Instalando e iniciando o server rabbit:

Como utilizaremos o rabbit em um container dentro do docker será necessário 
instalar a imagem com o comando abaixo:

`docker run -d --hostname my-rabbit --name rabbit13 -p 8080:15672 -p 5672:5672 -p 25676:25676 rabbitmq:3-management`

Agora para verificar se o RabbitMQ está rodando corretamente, acesse o seguinte endereço no seu navegador: http://localhost:8080/, em seguida logue com os dados de acesso:

```
 user:  guest
 senha: guest
```

# Instalando dependências do projeto:

Antes de iniciar instale as dependências do projeto:

`yarn install`

ou

`npm install`

# Rodando o projeto?

Para criar o worker execute o comando abaixo em uma instância do terminal:

`node worker.js`

Agora vamos criar a aplicação que envia a mensagem para fila com o comando abaixo:

`node app.js`

Agora no console ou na plataforma do rabbit é prossivel observar o fluxo das mensagens!
