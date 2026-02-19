# 🚀 API de Clientes - Spring Boot (GOF Project)

Projeto desenvolvido durante os estudos de padrões de projeto (GoF) na Digital Innovation One.

A aplicação é uma API REST para gerenciamento de clientes, com integração externa para busca automática de endereço via CEP (ViaCEP).

---

## 🧱 Arquitetura e Padrões

O projeto aplica boas práticas de arquitetura e separação de responsabilidades:

- Controller Layer (REST)
- Service Layer
- Repository Layer (Spring Data JPA)
- DTOs
- Exception Handling global
- Integração com API externa via OpenFeign

### Padrões utilizados

- Singleton (Beans Spring)
- Strategy (Service Layer)
- Facade (Integração ViaCEP)
- Dependency Injection

---

## 🔧 Tecnologias Utilizadas

- Java
- Spring Boot
- Spring Data JPA
- OpenFeign
- H2 Database
- Maven

---

## 📌 Funcionalidades

- Criar cliente
- Buscar cliente por ID
- Listar todos os clientes
- Atualizar cliente
- Deletar cliente
- Integração automática com ViaCEP ao cadastrar cliente
- Tratamento global de exceções (404 personalizado)

---

## 🌐 Endpoints

### 🔍 Buscar todos
GET /clientes

### 🔎 Buscar por ID
GET /clientes/{id}

### ➕ Criar cliente
POST /clientes

### ✏ Atualizar cliente
PUT /clientes/{id}

### ❌ Deletar cliente
DELETE /clientes/{id}

---

## ⚠️ Tratamento de Erros

Quando um cliente não é encontrado, a API retorna:

{
  "timestamp": "2024-01-01T12:00:00Z",
  "status": 404,
  "error": "Not Found",
  "message": "Cliente não encontrado com id: X"
}

---

## ▶️ Como executar

1. Clone o repositório

git clone https://github.com/Gustavo-Oliveira7/gofProject.git

2. Execute a aplicação

mvn spring-boot:run

3. Acesse:

http://localhost:8080/clientes

---
