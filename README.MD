# Websockets - Conexões Persistentes
### Take Blip - DIO


<h3>💻 Sobre:</h3>

    Projeto de estudo realizado no evento Tech Boost DIO. Foi utilizado websocket, uma tecnologia que permite a comunicação bidirecional por canais full-duplex sobre um único soquete Transmission Control Protocol (TCP).

<h3>✅ Recursos Utilizados:</h3>

- Visual Studio Code
- Javascript
- Razor
- .Net

<h3>✅ Criando o Chat:</h3>

1. Passos para criar o Servidor:

```
> dotnet new sln -n Chat-Websocket - criar a solution
> dotnet new mvc -o Server - criar um projeto mvc
> dotnet sln Chat-Websocket.sln add Server\Server.csproj - inserindo o projeto a solution
> cd .\Server\ - acessar a pasta 
> dotnet watch run  - executar o servidor

Acessar a pasta Properties/launchSettings.json configurar o "iisSettings" e "Client" com o "applicationUrl": "http://localhost:54985" e "sslPort": 0 evitar conflito com as portas utilizadas pelo Client.

Criar a pasta WebSocketManager, para criação das classes:
- WebSocketHandler.cs
- WebSocketManagerExtensions.cs
- WebSocketManagerMiddleware.cs

Criar a classe ChatHandler.cs na raiz do projeto

Acessar a classe startup.cs para configuração da Injeção de dependências, ativar o uso de websockets e configura a rota /ws
 
```

2. Passos para criar o Cliente:

```
> dotnet new mvc -o Client - criar um projeto mvc
> dotnet sln Chat-Websocket.sln add Client\Client.csproj - add o projeto a solution
> cd Client - acessar a pasta
> dotnet watch run - executar o Cliente

Acessar a pasta Properties/launchSettings.json para configurar o "iisSettings" e "Client" com o "applicationUrl": "http://localhost:5005" com as portas iguais.

Acessar a pasta wwwrot/js e criar o arquivo ChatServie.js e edição do site.js, responsáveis por realizar a conexão do cliente com o servidor.

Editar  o arquivo ChatServie.js adicionando a porta do websoket utilizada no Servidor e inserirna uri = "ws://localhost:54985/ws";

Acessar Views/Shared/_Layout para incluir ChatServie.js

```

<h3>✅ Autor:</h3>

Fábio Cavadas

Linkedin:  [br.linkedin.com/in/fábiocavadas](https://www.linkedin.com/in/fábiocavadas)

Github:  [github.com/FabioCavadas](https://github.com/FabioCavadas)


<h4> Desenvolvido por Fábio Cavadas<h4>