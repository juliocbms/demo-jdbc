#  Projeto de CRUD com JDBC e Padrão DAO

Este é um projeto de estudo em Java que implementa as operações básicas de um CRUD (Create, Read, Update, Delete) utilizando a API JDBC e o padrão de projeto **DAO (Data Access Object)**. Ele simula um sistema de gerenciamento de vendedores (*Sellers*) e departamentos (*Departments*), com interação direta ao banco de dados MySQL.

---

##  Objetivo

- Aprender o uso da API JDBC com conexão real a banco de dados
- Implementar o padrão DAO para separação de responsabilidades
- Manipular dados usando Java com PreparedStatements, ResultSet e transações
- Utilizar boas práticas de encapsulamento e reaproveitamento de código

---

##  Tecnologias Utilizadas

- **Java**
- **JDBC API**
- **MySQL**

---

##  Estrutura do Projeto
/src
├── application/
│ └── Main.java
├── db/
│ ├── DB.java
│ ├── DbException.java
│ └── DbIntegrityException.java
├── model/
│ ├── entities/
│ │ ├── Department.java
│ │ └── Seller.java
│ ├── dao/
│ │ ├── DaoFactory.java
│ │ ├── DepartmentDao.java
│ │ └── SellerDao.java
│ └── dao/impl/
│ └── SellerDaoJDBC.java
db.properties 


---

##  Funcionalidades

- `findById(id)`: Buscar vendedor por ID
- `findByDepartment(department)`: Buscar todos os vendedores de um departamento
- `findAll()`: Listar todos os vendedores
- `insert(obj)`: Inserir novo vendedor
- `update(obj)`: Atualizar dados de um vendedor
- `deleteById(id)`: Remover vendedor por ID

---

## Testes no Main.java
O arquivo Main.java possui os seguintes testes para validação dos métodos DAO:

 - Test 1: Buscar vendedor por ID
 - Test 2: Buscar vendedores por departamento
 - Test 3: Listar todos os vendedores
 - Test 4: Inserir novo vendedor
 - Test 5: Atualizar vendedor existente
 - Test 6: Deletar vendedor por ID

Basta descomentar os blocos e executar para validar.

## Boas Práticas Aplicadas
- Encapsulamento das regras de acesso a dados com o padrão DAO
- Separação clara entre camadas de aplicação
- Reaproveitamento de conexões e instâncias
- Manipulação segura de SQL com PreparedStatement

## Aprendizados
- Padrão de projeto DAO
- Programação orientada a objetos
- Tratamento de exceções customizadas
- Uso correto de ResultSet, Statements e transações

