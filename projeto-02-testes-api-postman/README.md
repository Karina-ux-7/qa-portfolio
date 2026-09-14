# Projeto 02 - Testes de API com Postman

Projeto prático de testes de API realizado com Postman utilizando a API pública Restful Booker.

## Objetivo

Praticar testes de API REST por meio de requisições HTTP, validação de respostas, manipulação de dados em JSON e análise de cenários positivos e negativos.

## Cenários executados

### CT-API-001 - Listar reservas

Método: `GET`

Objetivo: validar a consulta da lista de reservas disponíveis.

Resultado esperado:
retorno da requisição com sucesso e status `200 OK`.

Resultado obtido:
requisição executada com sucesso.

Status: Aprovado.

### CT-API-002 - Criar reserva

Método: `POST`

Objetivo: validar a criação de uma nova reserva enviando dados em formato JSON.

Dados utilizados:

- nome
- sobrenome
- valor da reserva
- status do depósito
- data de check-in
- data de check-out
- necessidade adicional

Resultado esperado:
criação da reserva e retorno de um identificador.

Resultado obtido:
reserva criada com sucesso e `bookingid` retornado pela API.

Status: Aprovado.

### CT-API-003 - Consultar reserva por ID

Método: `GET`

Objetivo: consultar uma reserva específica utilizando o `bookingid` retornado anteriormente.

Resultado esperado:
retorno dos dados correspondentes à reserva criada.

Resultado obtido:
dados da reserva retornados corretamente.

Status: Aprovado.

### CT-API-004 - Atualizar reserva

Método: `PUT`

Objetivo: validar a atualização completa dos dados de uma reserva.

Durante a execução, a API retornou inicialmente `403 Forbidden`, indicando falta de autorização para realizar a operação.

Após validar a autenticação, a atualização foi realizada com sucesso.

Status: Aprovado.

### CT-API-004A - Gerar token de autenticação

Método: `POST`

Endpoint utilizado: `/auth`

Objetivo: validar a geração de token utilizando credenciais de autenticação.

As credenciais foram configuradas por meio de variáveis no Postman para evitar exposição direta no arquivo exportado.

Resultado esperado:
retorno de token válido.

Resultado obtido:
token gerado com sucesso e status `200 OK`.

Status: Aprovado.

### CT-API-005 - Validar PATCH não permitido

Método: `PATCH`

Objetivo: verificar o comportamento da API ao tentar realizar uma atualização parcial no endpoint utilizado.

Resultado esperado:
identificar o comportamento da API para o método.

Resultado obtido:
`405 Method Not Allowed`.

Status: Aprovado como cenário negativo.

### CT-API-006 - Validar DELETE não permitido

Método: `DELETE`

Objetivo: verificar o comportamento da API ao tentar excluir uma reserva no endpoint utilizado.

Resultado obtido:
`405 Method Not Allowed`.

Status: Aprovado como cenário negativo.

### CT-API-007 - Consultar reserva inexistente

Método: `GET`

Objetivo: validar a resposta da API ao consultar um identificador de reserva inexistente.

Resultado esperado:
`404 Not Found`.

Resultado obtido:
`404 Not Found`.

Status: Aprovado.

## Conceitos praticados

- API REST
- endpoints
- métodos HTTP
- GET
- POST
- PUT
- PATCH
- DELETE
- JSON
- request
- response
- status codes
- autenticação
- token
- Basic Auth
- variáveis no Postman
- cenários positivos
- cenários negativos
- análise de respostas da API

## Status codes analisados

- `200 OK`
- `403 Forbidden`
- `404 Not Found`
- `405 Method Not Allowed`

## Ferramenta utilizada

Postman

## API utilizada

Restful Booker

https://restful-booker.herokuapp.com/

## Collection

A collection utilizada durante os testes está disponível neste diretório:

`Projeto 02 - Testes de API - Restful Booker.postman_collection.json`

As credenciais reais não foram incluídas no arquivo exportado.

## Resultado do projeto

O projeto permitiu praticar um fluxo de testes de API envolvendo criação, consulta, atualização, autenticação e validação de comportamentos de erro.

Também foram analisados cenários em que a resposta da API não correspondia a uma operação de sucesso, utilizando os status codes para entender o comportamento apresentado pelo serviço.

## Status

Concluído como projeto de estudo.

O projeto poderá receber novos cenários e melhorias conforme minha evolução em testes de API.

---

Karina
