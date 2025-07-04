# faws5.0
## Rodar a BIA local
### Dentro do diretorio
```
docker compose up -d
```
```
docker ps
```
```
http://localhost:3001/
```
### Mudar no docker file da BIA REACT_APP_API_URL=http://34.239.240.133 para REACT_APP_API_URL=http://localhost:3001
### Baixar o projeto
```
docker compose down
```
### Gerar uma nova imagem
```
docker compose build server
```
### Subir novamente o projeto
```
docker compose up -d
```
#### Para rodar as migrations no container ####
```
docker compose exec server bash -c 'npx sequelize db:migrate'
```
### Testar adicionar a tarefa no brower