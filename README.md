# Spring Security 6 - Implmentação 

Este é um projeto em Java que implementa um sistema de autenticação usando Spring Boot 3+, Spring Data JPA, Spring Security, Spring Web e OAuth2Resource. Ele permite que os usuários façam login ou se registrem por meio de requisições HTTP POST e, em seguida, acessem endpoints com base em suas funções.

Os usuários são autenticados em um banco de dados usando um `UserDetailsService` personalizado e um `AuthenticationManager`, juntamente com os repositórios do Spring Data JPA.

Quando o login é bem-sucedido, é gerado um JWT (JSON Web Token) e enviado de volta ao usuário. O usuário pode usar esse JWT no cabeçalho das requisições como um token de portador para acessar rotas autenticadas de acordo com suas funções.

## Recursos Principais

- Autenticação de usuário com senha usando PasswordEncoder.
- Uso do algoritmo Bcrypt para armazenar senhas com segurança.
- Geração e uso de JSON Web Tokens (JWT) para autenticação.
- Armazenamento e gerenciamento de chaves públicas JWK (JSON Web Key).

## Tecnologias Utilizadas

* ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.5.3-brightgreen)
* ![Spring Security](https://img.shields.io/badge/Spring%20Security-5.5.1-blue)
* ![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-2.5.3-blue)
* ![Spring Web](https://img.shields.io/badge/Spring%20Web-5.3.10-blue)
* ![OAuth2Resource](https://img.shields.io/badge/OAuth2Resource-2.5.3-blue)
* ![Bcrypt](https://img.shields.io/badge/Bcrypt-Segurança%20de%20Senhas-green)
* ![JWT](https://img.shields.io/badge/JWT-JSON%20Web%20Token-orange)

## Configuração

1. Clone o repositório para a sua máquina local.
2. Configure as informações do banco de dados no arquivo `application.properties` ou `application.yml`.
3. Execute a aplicação Spring Boot.

## Endpoints

A seguir estão alguns dos principais endpoints disponíveis na aplicação:

- `/auth/login`: Endpoint para autenticar usuários e gerar um JWT.
- `/auth/register`: Endpoint para registrar novos usuários.
- `/api/user`: Endpoint acessível apenas a usuários autenticados com a função de "usuário".
- `/api/admin`: Endpoint acessível apenas a usuários autenticados com a função de "administrador".

## Uso (Postman/Insomnia) 

1. Faça uma solicitação POST para `/auth/register` para criar uma nova conta.
2. Faça uma solicitação POST para `/auth/login` com as credenciais para obter um JWT.
3. Inclua o JWT no cabeçalho das solicitações para acessar endpoints protegidos.

## Autor

* Autor: Lucas Alves
* Email: [Lucas Alves](mailto:lkab05@hotmail.com)








