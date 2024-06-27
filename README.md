# Projeto de Exemplo: Padrões de Projeto com Spring Boot

Este projeto demonstra a implementação de padrões de projeto utilizando Spring Boot. O projeto inclui uma API REST para gerenciar clientes e endereços, integração com um banco de dados H2 e consumo da API externa ViaCEP utilizando OpenFeign.

## Tecnologias Utilizadas

- Java 17
- Spring Boot 2.5.4
- Spring Data JPA
- Spring Web
- Spring Cloud OpenFeign
- H2 Database
- OpenAPI/Swagger

## Estrutura do Projeto

### Pacotes e Classes Principais

- `one.digitalinnovation.gof.controller`
  - **ClienteRestController**: Controlador REST que fornece endpoints para operações CRUD de clientes.
  
- `one.digitalinnovation.gof.model`
  - **Cliente**: Entidade JPA que representa um cliente.
  - **Endereco**: Entidade JPA que representa um endereço.
  - **ClienteRepository**: Interface para operações CRUD no banco de dados para a entidade Cliente.
  - **EnderecoRepository**: Interface para operações CRUD no banco de dados para a entidade Endereco.

- `one.digitalinnovation.gof.service`
  - **ClienteService**: Interface que define métodos para operações CRUD de clientes.
  - **ViaCepService**: Interface Feign Client para consumir a API ViaCEP.

## Endpoints da API

### Clientes

- `GET /clientes`: Retorna todos os clientes.
- `GET /clientes/{id}`: Retorna um cliente específico pelo ID.
- `POST /clientes`: Insere um novo cliente.
- `PUT /clientes/{id}`: Atualiza um cliente existente.
- `DELETE /clientes/{id}`: Deleta um cliente pelo ID.
