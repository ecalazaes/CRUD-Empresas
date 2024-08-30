# API REST de Empresas

Este repositório contém uma API REST desenvolvida com Spring Boot versão 3.3.2, implementando um CRUD completo para gerenciamento de empresas. 
A aplicação segue uma arquitetura em camadas, com as camadas Controller, Service, Repository e Entidades.

## Tecnologias Utilizadas

- **Spring Boot 3.3.3**: Framework principal para construção da API.
- **JPA & Hibernate**: Para mapeamento objeto-relacional e persistência de dados.
- **MySQL**: Banco de dados utilizado para armazenar as informações das empresas.
- **Bean Validation**: Para validação dos dados da entidade Empresa.
- **Postman**: Utilizado para testar e validar os endpoints da API.
- **Swagger**: Para documentação interativa dos endpoints da API.

## Estrutura do Projeto

O projeto segue uma arquitetura tradicional em camadas:

- **Controller**: Responsável por receber as requisições HTTP e retornar as respostas.
- **Service**: Contém a lógica de negócios da aplicação.
- **Repository**: Camada de acesso a dados, utilizando Spring Data JPA.
- **Entidades**: Representam os objetos de domínio, mapeados para as tabelas do banco de dados.

## Endpoints Disponíveis 

### Empresas

- **GET /produtos**: Retorna todos os produtos.
  - **Resposta**: `200 OK`
  ```json
  [
    {
      "id": 20,
      "nome": "Empresa Teste1",
      "cnpj": "14275282000144",
      "email": "empretateste1@gmail.com"
    },
    {
      "id": 21,
      "nome": "Empresa Teste2",
      "cnpj": "14275282000225",
      "email": "empretateste2@gmail.com"
    }
  ]

## Documentação Swagger
A API está documentada utilizando Swagger, permitindo que você explore os endpoints e teste as requisições diretamente do navegador.

- URL de acesso: http://localhost:8080/api  
<br>![Swagger](img/swagger.png)

## Banco de Dados H2
A aplicação utiliza o banco de dados em memória H2 para testes. Você pode acessar a interface web do H2 para inspecionar as tabelas e dados persistidos.

- URL de acesso: http://localhost:8080/h2-console
- JDBC URL: jdbc:h2:mem:testdb
- Username: sa
- Password: (deixe em branco)

## Como Executar
1. Clone o repositório
   ```bash
   https://github.com/ecalazaes/CRUD-Produtos.git
   
2. Navegue até o diretório do projeto:
   ```bash
   cd CRUD-Produtos
  
3. Execute o projeto:
   ```bash
   ./mvnw spring-boot:run

4. Acesse a API no endereço:
   ```bash
   http://localhost:8080/produtos
   ```
   
   ```bash
   http://localhost:8080/categorias

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
