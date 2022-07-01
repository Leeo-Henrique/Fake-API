# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Produto

GET /products <br/>
POST /products <br/>
PATCH /products/IDPRODUTO <br/>
DELETE /products/IDPRODUTO

A rota produto o cliente deve conter um token de autenticaçao,

Criando um produto <br/>
`POST /products `

```json
{
  "product_Name": "Pizza mussarela",
  "price": 20,
  "userId": "Id user registrado",
  "image": "https://static7.depositphotos.com/1011415/743/v/600/depositphotos_7438540-stock-illustration-cheeseburger.jpg"
}
```

PATCH /products/IDPRODUTO <br/>
Editando um produto existente <br/>

PATCH /products/IDPRODUTO <br/>

```json
{
  "product_Name": "Pizza mussarela",
  "price": 36,
  "userId": "Id user registrado",
  "image": "https://static7.depositphotos.com/1011415/743/v/600/depositphotos_7438540-stock-illustration-cheeseburger.jpg"
}
```

Deletar um produto

`DELETE /products/IDPRODUTO `

```json
{
  "auth": "Bearer"
}
```

Todos os produtos
GET /products <br/>

```json
{
  "auth": "Bearer"
}
```
