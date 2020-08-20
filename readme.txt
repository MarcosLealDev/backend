?@Daniele Leao Evangelista  INPUT MASK

Node
Call Stack
C++ libuv (multi-processors)
Background threads
Non-blocking I/O

Framework
  *ExpressJS (microFramework)
	- micro serviços
  *Adonis
  *NextJS

Fluxo de Requisição
 * Client request
 * Answer with data structure
 * Client received and process results

Rotas HTTP:
 * GET  http://app.com/users
 * POST http://app.com/users
 * PUT  http://app.com/users/1
 * DELETE http://app.com/users/1

Benefícios:
 * Multiplos clientes
 * protocolo padronizado

JSON (JavaScript Object Notation)

GET
* Route		http://app.com/users
* Route Params	http://app.com/users/1/
* Query Params	http://app.com/users/1/?page=2

POST
http://app.com/users/1/
Body
{
  "user": {
     "name": "Diego Fernandes"
     "email": "diego@rocketseat.com
     "tech": ["ReactJS", "NodeJS]"
}
Header
{
  "Locale":"pt_BR"
}

HTTP codes:
1xx: Informational
2xx: Sucess
  * 200: sucess
  * 201: created
3xx: Redirection
  * 301: moved permanently
  * 302: moved
4xx: Client Errors
  * 400: bad request
  * 401: unauthorized
  * 404: not found
5xx: Server Errors
  * 500: internal server error

Começando um projeto:

yarn init -y
yarn add express

Pra executar, rodar primeiro
node src/index.js  
mas tem que cancelar e rodar de novo se trocar c'odigo

Para todar direto
yarn add nodemon -D
e rodar
yarn nodemon src/index.js

Ou Editar package.json
main: "src/index.js"
script: {dev: "nodemon"}


Métodos HTTP:
GET: Buscar informação do back-end
POST: Criar uma informação no back-end
PUT/PATCH: Alterar uma infromação no back-end
DELETE: Deletar uma informação no back-end

Tipos de Parametros:
Query Params: Filters and Pagination http://localhost:3333/projects?title=react&owner=Diego
Route Params: Identificar recursos (Atualizar/Deletar) http://localhost:3333/1
Request Body: Conteúdo na hora de criar ou editar um recurso (JSON)

another lib to create IDs
yarn add uuidv4
And into the code
const {uuid} require('uuidv4')


Middleware:
Interceptador de requisições que interromper totalmente ou alterar dados da requisição.
