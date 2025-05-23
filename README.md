# 📋 Task Manager API

API REST completa para gerenciamento de tarefas (CRUD + filtros + estatísticas), construída com Java 17 e Spring Boot 3. Ideal para estudos, testes e protótipos rápidos com banco em memória H2.

---

## 🚀 Funcionalidades

* ✅ CRUD completo de tarefas
* 🔍 Filtros por status (`completed`) e data (`dueBefore`)
* 📊 Contador de tarefas (total, pendentes, concluídas)
* ✔️ Marcar tarefa como concluída
* 🧪 Validações com mensagens claras de erro
* 🔎 Documentação automática via Swagger/OpenAPI
* 💾 Banco H2 em memória com console web

---

## 🛠 Tecnologias

* Java 17
* Spring Boot 3
* Spring Web
* Spring Data JPA
* H2 Database (in-memory)
* Jakarta Validation
* SpringDoc OpenAPI (Swagger UI)

---

## ▶️ Como rodar o projeto

1. Clone o repositório:

```bash
git clone <url-do-seu-repositorio>
cd taskmanager
```

2. Execute o projeto com Maven:

```bash
mvn spring-boot:run
```

3. Acesse os principais recursos:

* 📚 Swagger UI: [`http://localhost:8080/swagger-ui.html`](http://localhost:8080/swagger-ui.html)
* 📂 Lista de tarefas: `GET http://localhost:8080/tasks`
* 🧠 Console do H2: [`http://localhost:8080/h2-console`](http://localhost:8080/h2-console)

---

## 📌 Endpoints principais

| Método | Rota                          | Descrição                              |
| ------ | ----------------------------- | -------------------------------------- |
| GET    | `/tasks`                      | Lista todas as tarefas                 |
| GET    | `/tasks?completed=true`       | Filtra tarefas concluídas              |
| GET    | `/tasks?dueBefore=2025-06-01` | Filtra tarefas com prazo antes da data |
| GET    | `/tasks/count`                | Retorna total, concluídas e pendentes  |
| GET    | `/tasks/{id}`                 | Busca uma tarefa por ID                |
| POST   | `/tasks`                      | Cria nova tarefa                       |
| PUT    | `/tasks/{id}`                 | Atualiza uma tarefa existente          |
| PATCH  | `/tasks/{id}/complete`        | Marca tarefa como concluída            |
| DELETE | `/tasks/{id}`                 | Remove uma tarefa                      |

---

## 🗃️ Configuração do banco H2

Banco em memória ativado automaticamente ao rodar o projeto.

* URL: `jdbc:h2:mem:taskdb`
* Usuário: `sa`
* Senha: *(em branco)*
* Acesse: [`http://localhost:8080/h2-console`](http://localhost:8080/h2-console)

---

## 📈 Melhorias futuras

* 🔐 Autenticação (JWT ou OAuth2)
* 🗃️ Integração com banco externo (PostgreSQL, MySQL)
* ✅ Testes unitários e de integração (JUnit + Testcontainers)
* ☁️ Deploy em nuvem (Render, Railway, Heroku)
