# CLI 

### Linux:
```
sudo docker run -d -i -t -p 15432:5432 -e POSTGRES_PASSWORD=yourPass postgres:13
```
_Via CLI não é a maneira comum de se fazer, mas para caso queira entender como o fazer, aí está._

# Explicando e usando [Docker-compose](https://docs.docker.com/compose/). 

O Docker compose, nada mais é que uma forma de orquestrar containers Docker. Ele possui um arquivo ```docker-compose.yml``` que será o responsável pela configuração e documentação das dependências do nosso projeto. 


## Exemplo de um arquivo docker-compose.yml: 

```
version: '3.5'

services: 
  database:
    image: postgres:12
    ports: 
      - 15432:5432
    environment:
      - POSTGRES_PASSWORD=@YourPassword123
```