📝 TODO API

API REST para gerenciamento de tarefas (TODO list) desenvolvida com Spring Boot.

🚀 Tecnologias

Java 17+
Spring Boot
Maven
Spring Web
Spring Data JPA (presumido)

📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

Java JDK 17 ou superior
Maven 3.6+
Git

🔧 Instalação

1. Clone o repositório

  git clone https://github.com/seu-usuario/todo-api.git
  cd todo-api

2. Compile o projeto
   
   mvn clean install

3. Execute a aplicação

  mvn spring-boot:run

A API estará disponível em: http://localhost:8080

📚 Endpoints

Criar Tarefa

POST /tarefas
Content-Type: application/json

{
  "descricao": "Estudar Java"
}

Exemplo com curl:

curl -X POST http://localhost:8080/tarefas \
  -H "Content-Type: application/json" \
  -d '{"descricao":"Estudar Java"}'

Listar Todas as Tarefas

GET /tarefas

Exemplo com curl:

curl http://localhost:8080/tarefas

Atualizar Tarefa

PUT /tarefas/{id}
Content-Type: application/json

{
  "descricao": "Estudar Spring Boot",
  "concluida": true
}

Exemplo com curl:

curl -X PUT http://localhost:8080/tarefas/1 \
  -H "Content-Type: application/json" \
  -d '{"descricao":"Estudar Spring Boot","concluida":true}'


Deletar Tarefa

DELETE /tarefas/{id}

Exemplo com curl:

curl -X DELETE http://localhost:8080/tarefas/1



