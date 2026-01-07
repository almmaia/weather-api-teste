 Weather API - Teste Técnico

API REST desenvolvida em Java (Spring Boot) para consulta de dados climáticos, utilizando banco de dados PostgreSQL e conteinerização com Docker.

Tecnologias Utilizadas

Linguagem: Java 21
Framework: Spring Boot 3
Banco de Dados: PostgreSQL
Container: Docker & Docker Compose
Documentação: Swagger (OpenAPI)

Como Rodar o Projeto

Este projeto utiliza Docker para garantir que funcione em qualquer máquina sem necessidade de instalar Java ou Banco de Dados localmente.

Pré-requisitos
Docker e Docker Compose instalados.
Git instalado.

Passo a Passo

1.  Clone o repositório:**
    ```bash
    git clone [https://github.com/almmaia/weather-api-teste.git](https://github.com/almmaia/weather-api-teste.git)
    cd weather-api-teste


2.  Suba o ambiente (API + Banco):
    bash
    docker-compose up --build
    
    Aguarde até aparecer a mensagem "Started WeatherApiApplication" no terminal.

Como Acessar e Testar

1. Documentação Interativa (Swagger)
Acesse pelo navegador para visualizar todos os endpoints e testar sem instalar nada:
[http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

Endpoints Principais

Consultar Clima (POST):
    URL: http://localhost:8080/weather/{cidade}
    Exemplo:http://localhost:8080/weather/London

Estrutura do Banco de Dados
O projeto utiliza o PostgreSQL. As tabelas são geradas automaticamente pelo Hibernate (JPA) ao iniciar a aplicação.
Tabela: `weather_entity` (Armazena histórico de consultas).
