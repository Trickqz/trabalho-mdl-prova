# Sistema Bancário - Modelo Conceitual e Relacional

## Descrição do Projeto

Este projeto visa desenvolver e implementar um banco de dados robusto para um sistema bancário, baseando-se nos modelos conceitual e relacional. O objetivo é organizar e estruturar os dados essenciais das operações bancárias, proporcionando uma base sólida para o gerenciamento eficiente e seguro das informações críticas.

## Estrutura do Projeto

O projeto está dividido nas seguintes seções:

1. **Modelo Conceitual**: 
   - Diagrama Entidade-Relacionamento (ER)
   - Descrição das entidades e seus atributos
   - Relacionamentos entre entidades

2. **Modelo Relacional**: 
   - Tabelas relacionais derivadas do modelo conceitual
   - Definição de chaves primárias e estrangeiras

## Entidades Principais

### Cliente
Representa uma pessoa que utiliza os serviços do banco.
- **Atributos**:
  - ID (Chave Primária)
  - Nome
  - Endereço
  - Telefone
  - E-mail
  - Data de Nascimento

### Conta
Representa uma conta bancária.
- **Atributos**:
  - Número da Conta (Chave Primária)
  - Tipo de Conta
  - Saldo
  - ID do Cliente (Chave Estrangeira)

### Transação
Registra operações financeiras.
- **Atributos**:
  - ID (Chave Primária)
  - Data
  - Tipo (Depósito, Saque, Transferência)
  - Valor
  - Conta de Origem (Chave Estrangeira)
  - Conta de Destino (Chave Estrangeira, pode ser nula para saques)

### Empréstimo
Representa um empréstimo concedido pelo banco.
- **Atributos**:
  - ID (Chave Primária)
  - Data do Empréstimo
  - Valor
  - Taxa de Juros
  - Data de Vencimento
  - Número da Conta (Chave Estrangeira)

## Relacionamentos

- **Cliente - Conta**: Um cliente pode ter uma conta.
- **Conta - Transação**: Uma conta pode ter várias transações.
- **Conta - Empréstimo**: Uma conta pode ter vários empréstimos.

## Diagramas

### Diagrama ER Completo
![Diagrama ER](path/to/diagrama_er.png)

### Diagrama Relacional
![Diagrama Relacional](path/to/diagrama_relacional.png)
