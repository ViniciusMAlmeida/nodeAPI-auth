# Aula 09 - Variáveis de Ambiente e Dotenv

## Dependencias do projeto:

npm i nodemon sequelize-cli -D

npm i express pg pg-hstore sequelize jsonwebtoken bcryptjs express-async-errors dotenv
<br><br>

## Configuração do projeto:

acessar diretório `./src/db` e rodar o comando `npx sequelize-cli init`

mudar a extensão do arquivo ./src/db/config/config.json para `.js` e exportar o
objeto de configuração

criar um arquivo `.sequelizerc` na raiz do projeto, configurar o path dos
diretórios

alterar a extensão (.json para .js) do arquivo de configuração `/src/db/models/index.js`
na linha 8, variável `config`
<br><br>

## Comandos do sequelize-cli:

criar migration
`npx sequelize-cli model:generate --name User --attributes firstName:string,lastName:string,email:string`

rodar migration
`npx sequelize-cli db:migrate`

desfazer migration
`npx sequelize-cli db:migrate:undo`


## Passos da aula

Partindo da aula anterior: <br>
Importar a lib `dotenv` e execute-a na primeira linha do arquivo `server.js`<br>
Adicione uma regra de exceção no arquivo `.gitignore` apontando para o arquivo `.env`<br>
Crie um arquivo `.env-example` e um `.env` na raiz do projeto <br>
No arquivo `.env` crie as variáveis de ambiente para substituir os dados sensíveis do projeto (credenciais do banco de dados e chave JWT) <br>
Navegue nos arquivos onde esses dados se encontram e substua seus valores utilizando as variáveis de ambiente <br>
