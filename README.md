# json-server-base

Esse é o meu json server.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /login <br/>
POST /vehicles <br/>
POST /animals

O register serve para cadastrar usuários.
Vehicles serve para cadastrar novos veículos, no corpo apenas necessário model (modelo) e brand (marca). Necessário o token de login para a criação de um novo veículo.
Animals serve para cadastrar novos animais, no corpo apoenas type, name e userID. Necessário o token de login para a criação de um novo animal.

### Login

POST /login

Endpoint usado para realizar login com um dos usuários cadastrados na lista de "Users".

### Get

GET /vehicles
GET /users
GET /animals

Utilize o token de acesso para ver os veículos cadastrados.
Utilize o token de acesso, e o id do usuário na barra de endereço para ver as informações do usuário.
A requisição get animals não necessita de token.
