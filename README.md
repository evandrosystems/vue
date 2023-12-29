# VUE CLI

Este repositório fornece uma estrutura Docker com Docker Compose otimizada para projetos Vue CLI. Clone este repositório e utilize essa configuração pronta para acelerar o início de seus projetos front-end Vue CLI, simplificando o processo de desenvolvimento.

#### Como usar?

##### 1º Criando o .env
Copie o arquivo __".env-example"__ e crie outro chamado __".env"__ </div>
```
cp .env-example .env
```

##### 2º Criando a imagem
```
docker compose build --no-cache
```

##### 3º Criando o container
Fique atento ao nome do serviço no docker-compose.yml </div>
Nesse repositório se chama __"vue"__
```
docker compose run --rm -it vue bash
```

##### 4º Criando o projeto vue cli
No passo anterior você criou e entrou dentro do container. </div>
Estando dentro do container com o passo anterior, agora vamos criar um projeto vue cli. </div>
```
create vue . --no-git
```
- Siga os passos e configure seu projeto com a versão que deseja do vue cli.
- Espere o projeto ser criado e transferido para o volume
- Depois para sair do container execute __"exit"__

##### 5º Dê permissões (Linux)
Se você usa linux talvez precise aplicar permissões a tudo que é criado dentro do container </div>
forneça seu usuário e grupo para aplicar permissões ou use outra maneira
```
sudo chown -R user:group .
```
Agora você pode acessar seu aplicativo vue cli, pelo navegador </div>
use a porta configurada no .env que por padrão é "8000"

##### 6º Executando o projeto
Depois de todos os passos anteriores, agora vamos -</div>
executar o projeto no navegador
```
docker compose up -d
```
Agora você pode acessar seu aplicativo vue cli, pelo navegador </div>
use a porta configurada no .env que por padrão é "8000"

[http://localhost:8000](http://localhost:8000) </br></br></br>

Depois faço mais atualizações.
###### Siga me!
###### Faça um fork para contribuir com o projeto, caso queira.
###### Me dê uma estrelinha.