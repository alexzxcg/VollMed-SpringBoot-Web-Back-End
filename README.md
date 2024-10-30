# Voll Med API
## Objetivo
> Este projeto tem como objetivo desenvolver uma API Rest para uma clínica médica fictícia chamada Voll Med.
O sistema permitirá o gerenciamento de médicos, pacientes e consultas, com funcionalidades completas de CRUD
(Create, Read, Update, Delete). Além disso, a API inclui:

- Funcionalidade de agendamento de consultas
- Validações de dados com Bean Validation;
- Paginação e ordenação de resultados;
- Aplicação de boas práticas de desenvolvimento utilizando Spring Boot 3 e Java 21 LTS.
- Tratamento de erros
- Autenticação/Autorização com Spring Security
- Tokens JWT
- Documentação da API
- Testes automatizados
- Build do projeto

## Requisitos

<details>
  <summary>Cadastro de Médicos</summary>

### Cadastro de Médicos  
O sistema deve possuir uma funcionalidade de cadastro de médicos, na qual as seguintes informações deverão ser preenchidas:  
- Nome  
- E-mail  
- Telefone  
- CRM  
- Especialidade (Ortopedia, Cardiologia, Ginecologia ou Dermatologia)  
- Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)  

**Observação**: Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.

</details>

<details>
  <summary>Listagem de Médicos</summary>

### Listagem de Médicos  
O sistema deve possuir uma funcionalidade de listagem de médicos, na qual as seguintes informações de cada um dos médicos cadastrados deverão ser exibidas:  
- Nome  
- E-mail  
- CRM  
- Especialidade  

A listagem deve ser ordenada pelo nome do médico, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.

</details>

<details>
  <summary>Atualização de Médicos</summary>

### Atualização de Médicos  
O sistema deve possuir uma funcionalidade de atualização de dados cadastrais de médicos, na qual as seguintes informações poderão ser atualizadas:  
- Nome  
- Telefone  
- Endereço  

</details>

<details>
  <summary>Exclusão de Médicos</summary>

### Exclusão de Médicos  
O sistema deve possuir uma funcionalidade que permita a exclusão de médicos cadastrados.  

**Observação**: A exclusão não deve apagar os dados do médico, mas torná-lo como "inativo" no sistema.

</details>

<details>
  <summary>Cadastro de Pacientes</summary>

### Cadastro de Pacientes  
O sistema deve possuir uma funcionalidade de cadastro de pacientes, na qual as seguintes informações deverão ser preenchidas:  
- Nome  
- E-mail  
- Telefone  
- CPF  
- Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)  

**Observação**: Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.

</details>

<details>
  <summary>Listagem de Pacientes</summary>

### Listagem de Pacientes  
O sistema deve possuir uma funcionalidade de listagem de pacientes, na qual as seguintes informações de cada um dos pacientes cadastrados deverão ser exibidas:  
- Nome  
- E-mail  
- CPF  

A listagem deve ser ordenada pelo nome do paciente, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.

</details>

<details>
  <summary>Atualização de Pacientes</summary>

### Atualização de Pacientes  
O sistema deve possuir uma funcionalidade de atualização de dados cadastrais de pacientes, na qual as seguintes informações poderão ser atualizadas:  
- Nome  
- Telefone  
- Endereço  

</details>

<details>
  <summary>Exclusão de Pacientes</summary>

### Exclusão de Pacientes  
O sistema deve possuir uma funcionalidade que permita a exclusão de pacientes cadastrados.  

**Observação**: A exclusão não deve apagar os dados do paciente, mas torná-lo como "inativo" no sistema.

</details>

<details>
  <summary>Agendamento de Consultas</summary>

### Agendamento de Consultas  
O sistema deve possuir uma funcionalidade que permita o agendamento de consultas, na qual as seguintes informações deverão ser preenchidas:  
- Paciente  
- Médico  
- Data/Hora da consulta  

**Observações**:  
- O horário de funcionamento da clínica é de segunda a sábado, das 07:00 às 19:00.  
- As consultas têm duração fixa de 1 hora.  
- As consultas devem ser agendadas com antecedência mínima de 30 minutos.

</details>

<details>
  <summary>Cancelamento de Consultas</summary>

### Cancelamento de Consultas  
O sistema deve possuir uma funcionalidade que permita o cancelamento de consultas, na qual as seguintes informações deverão ser preenchidas:  
- Consulta  
- Motivo do cancelamento  

**Observações**:  
- É obrigatório informar o motivo do cancelamento da consulta, dentre as opções:  
  - Paciente desistiu  
  - Médico cancelou  
  - Outros  
- Uma consulta somente poderá ser cancelada com antecedência mínima de 24 horas.

</details>

<details>
  <summary>Regras de Negócio</summary>

### Regras de Negócio  
- Não permitir a alteração do e-mail do médico.  
- Não permitir a alteração do CRM do médico.  
- Não permitir a alteração da especialidade do médico.  
- Não permitir a alteração do e-mail do paciente.  
- Não permitir a alteração do CPF do paciente.  
- Não permitir o agendamento de consultas com pacientes inativos no sistema.  
- Não permitir o agendamento de consultas com médicos inativos no sistema.  
- Não permitir o agendamento de mais de uma consulta no mesmo dia para um mesmo paciente.  
- Não permitir o agendamento de uma consulta com um médico que já possui outra consulta agendada na mesma data/hora.  
- A escolha do médico é opcional, sendo que, nesse caso, o sistema deve escolher aleatoriamente algum médico disponível na data/hora preenchida.

</details>

## Tecnologias Utilizadas

<details>
  <summary>Frameworks e Linguagens</summary>
  
  - [Spring Boot 3](https://spring.io/projects/spring-boot): Framework principal para construção da API.  
  - [Java 21](https://www.oracle.com/java/technologies/downloads/): Última versão LTS (Suporte de Longo Prazo) do Java.  

</details>

<details>
  <summary>Banco de Dados e Persistência</summary>
  
  - [MySQL](https://www.mysql.com/): Banco de dados relacional para armazenamento de informações.  
  - [JPA/Hibernate](https://hibernate.org/): Persistência de dados com suporte a ORM (Mapeamento Objeto-Relacional).  
  - [Flyway](https://flywaydb.org/): Controle de versionamento e migração do banco de dados.  

</details>

<details>
  <summary>Gerenciamento de Dependências e Build</summary>
  
  - [Maven](https://maven.apache.org/): Gerenciamento de dependências e build do projeto.  

</details>

<details>
  <summary>Testes Automatizados</summary>
  
  - [JUnit](https://junit.org/junit5/): Framework para testes automatizados e unitários, garantindo a integridade do código.  
  - [Mockito](https://site.mockito.org/): Biblioteca para criação de mocks e simulação de dependências em testes.  

</details>

<details>
  <summary>Segurança e Autenticação</summary>
  
  - [Spring Security](https://spring.io/projects/spring-security): Implementação de autenticação e autorização.  
  - [Auth0 - JWT](https://github.com/auth0/java-jwt): Utilizado para geração e validação de tokens JWT, proporcionando segurança adicional.  

</details>

<details>
  <summary>Ferramentas e Utilitários</summary>
  
  - [Lombok](https://projectlombok.org/): Redução de código repetitivo com anotações para geração de getters, setters, etc.  
  - [Insomnia](https://insomnia.rest/): Ferramenta para testar requisições da API.  

</details>

## Implementações Realizadas

<details>
  <summary>CRUD de Médicos e Pacientes</summary>

### CRUD de Médicos e Pacientes  
- Implementação completa seguindo os requisitos.
- Validação de campos obrigatórios com **Bean Validation**.
- Uso do padrão **DTO** para separar lógica de negócio.
- Persistência de dados com **JPA/Hibernate** e banco de dados **MySQL**.
- Exclusão lógica, tornando o médico/paciente inativo em vez de removê-lo.
- **Flyway** usado para versionamento e criação das tabelas de médicos e pacientes.

</details>

<details>
  <summary>Listagem de Médicos e Pacientes</summary>

### Listagem de Médicos e Pacientes  
- Implementada de acordo com os requisitos.
- Uso de **DTO** para exibir apenas as informações necessárias.
- **Paginação e ordenação** aplicadas usando a biblioteca **Pageable** do Spring Boot.
- Listagem com 10 registros por página e ordenação crescente pelo nome.

</details>

<details>
  <summary>Agendamento e Cancelamento de Consultas</summary>

### Agendamento e Cancelamento de Consultas  
- Lógica desenvolvida seguindo os requisitos e regras de negócio.
- Aplicação dos princípios **SOLID**:
  - **S**: Cada classe tem uma responsabilidade única.
  - **O**: Classes de validação abertas para extensão, fechadas para modificação.
  - **D**: Interface criada para representar o método de validação.
- Validações separadas em classes distintas, uma por regra de negócio.
- Uso de **interfaces** para flexibilidade e desacoplamento.

</details>

<details>
  <summary>Tratamento de Respostas HTTP</summary>

### Tratamento de Respostas HTTP  
- Ajustes nas controllers para garantir conformidade com o protocolo HTTP:
  - **201 Created**: Para recursos recém-criados.
  - **200 OK**: Para atualizações bem-sucedidas.
  - **204 No Content**: Para exclusões lógicas.
  - **404 Not Found** e **400 Method Argument Not Valid**: Tratamento de erros.

</details>

<details>
  <summary>Geração, Validação e Autenticação de Tokens JWT</summary>

### Geração, Validação e Autenticação de Tokens JWT  
- Implementado gerador e validador de tokens JWT com **Auth0** e **Spring Security**.
- Autenticação e controle de acesso usando **tokens JWT**.
- Configuração do **Spring Security** para proteger rotas.
- Verificação de token em cada requisição, proporcionando segurança adicional.

</details>

<details>
  <summary>Testes Automatizados</summary>

### Testes Automatizados  
- **JUnit** e **Mockito**: Usados para garantir a qualidade do sistema.
- **Testes na Controller**: Simulam chamadas à Controller que delega agendamento ao Service.
- **Testes no Médico Repository**: Verificam o método que escolhe aleatoriamente um médico disponível na data agendada.

</details>
