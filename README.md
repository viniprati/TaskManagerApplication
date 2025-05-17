# Task Manager API

API REST simples para gerenciar tarefas (CRUD) usando Java 17, Spring Boot 3, Spring Data JPA e banco em memória H2.

---

## Funcionalidades

* Criar, listar, atualizar e deletar tarefas
* Persistência com banco H2 em memória
* Documentação automática via Swagger/OpenAPI

---

## Tecnologias

* Java 17
* Spring Boot 3
* Spring Data JPA
* H2 Database (em memória)
* SpringDoc OpenAPI (Swagger UI)

---

## Rodando o projeto

1. Clone o repositório

```bash
git clone <url-do-seu-repositorio>
cd taskmanager
```

2. Execute via Maven

```bash
mvn spring-boot:run
```

3. Acesse a API

* Lista todas as tarefas: `GET http://localhost:8080/tasks`
* Documentação Swagger: `http://localhost:8080/swagger-ui.html`

---

## Endpoints principais

| Método | URL         | Descrição               |
| ------ | ----------- | ----------------------- |
| GET    | /tasks      | Listar todas as tarefas |
| GET    | /tasks/{id} | Buscar tarefa por ID    |
| POST   | /tasks      | Criar nova tarefa       |
| PUT    | /tasks/{id} | Atualizar tarefa        |
| DELETE | /tasks/{id} | Deletar tarefa          |

---

## Configuração do banco

Usa banco H2 em memória para facilitar testes sem necessidade de instalação.

Console H2 disponível em: `http://localhost:8080/h2-console`
(JDBC URL: `jdbc:h2:mem:taskdb`, usuário: `sa`, senha vazia)

---

## Melhorias futuras

* Adicionar autenticação
* Persistência com banco externo (PostgreSQL, MySQL)
* Testes unitários e integração
* Deploy em nuvem (Railway, Heroku, etc)
