# VUE CLI

Este repositório fornece uma estrutura Docker com Docker Compose otimizada para projetos Vue CLI. Clone este repositório e utilize essa configuração pronta para acelerar o início de seus projetos front-end Vue CLI, simplificando o processo de desenvolvimento.

#### Como usar?

#### 1º Criando o .env
Copie o arquivo __".env-example"__ e crie outro chamado __".env"__ </br>
```
cp .env-example .env
```

#### 2º Criando a imagem
```
docker compose build --no-cache
```

#### 3º Criando o container
Fique atento ao nome do serviço no docker-compose.yml </br>
Nesse repositório se chama __"vue"__
```
docker compose run --rm -it vue bash
```

#### 4º Criando o projeto vue cli
No passo anterior você criou e entrou dentro do container. </br>
Estando dentro do container com o passo anterior, agora vamos criar um projeto vue cli. </br>
```
create vue . --no-git
```
- Siga os passos e configure seu projeto com a versão que deseja do vue cli.
- Espere o projeto ser criado e transferido para o volume
- Agora você precisa sair do container, use o comando __"exit"__


#### 5º Executando o projeto
```
docker compose up -d
```
Agora você pode acessar seu aplicativo vue cli, pelo navegador </br>
use a porta configurada no .env que por padrão é "8000"

[http://localhost:8000](http://localhost:8000)