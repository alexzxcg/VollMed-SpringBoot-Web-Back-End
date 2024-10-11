# Voll Med API
## Objetivo
> Este projeto tem como objetivo desenvolver uma API Rest para uma clínica médica fictícia chamada Voll Med.
O sistema permitirá o gerenciamento de médicos, pacientes e consultas, com funcionalidades completas de CRUD
(Create, Read, Update, Delete). Além disso, a API inclui:

- Validações de dados com Bean Validation;
- Paginação e ordenação de resultados;
- Aplicação de boas práticas de desenvolvimento utilizando Spring Boot 3 e Java 21 LTS.

## Requisitos
- Cadastro de médicos:
O sistema deve possuir uma funcionalidade de cadastro de médicos, na qual as seguintes informações deverão ser preenchidas.
  - Nome
  - E-mail
  - Telefone
  - CRM
  - Especialidade (Ortopedia, Cardiologia, Ginecologia ou Dermatologia)
  - Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)
> Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.

- Listagem de médicos:
O sistema deve possuir uma funcionalidade de listagem de médicos, na qual as seguintes informações, de cada um dos médicos cadastrados, deverão ser exibidas.
  - Nome
  - E-mail
  - CRM
  - Especialidade
> A listagem deve ser ordenada pelo nome do médico, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.

- Atualização de médicos: o sistema deve possuir uma funcionalidade de atualização de dados cadastrais de médicos, na qual as seguintes informações poderão ser atualizadas
  - Nome
  - Telefone
  - Endereço

- Cadastro de pacientes: O sistema deve possuir uma funcionalidade de cadastro de pacientes, na qual as seguintes informações deverão ser preenchidas.
  - Nome
  - E-mail
  - Telefone
  - CPF
  - Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)
> Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.

- Listagem de pacientes: O sistema deve possuir uma funcionalidade de listagem de pacientes, na qual as seguintes informações, de cada um dos pacientes cadastrados, deverão ser exibidas.
  - Nome
  - E-mail
  - CPF
> A listagem deve ser ordenada pelo nome do paciente, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.

- Atualização de pacientes: O sistema deve possuir uma funcionalidade de atualização de dados cadastrais de pacientes, na qual as seguintes informações poderão ser atualizadas.
  - Nome
  - Telefone
  - Endereço

- Exclusão de pacientes: O sistema deve possuir uma funcionalidade que permita a exclusão de pacientes cadastrados.

- Agendamento de consultas: O sistema deve possuir uma funcionalidade que permita o agendamento de consultas, na qual as seguintes informações deverão ser preenchidas.
  - Paciente
  - Médico
  - Data/Hora da consulta

- Cancelamento de consultas: O sistema deve possuir uma funcionalidade que permita o cancelamento de consultas, na qual as seguintes informações deverão ser preenchidas
  - Consulta
  - Motivo do cancelamento
  
- As seguintes regras de negócio devem ser validadas pelo sistema:
  - Não permitir a alteração do e-mail do médico;
  - Não permitir a alteração do CRM do médico;
  - Não permitir a alteração da Especialidade do médico.
  - Não permitir a alteração do e-mail do paciente;
  - Não permitir a alteração do CPF do paciente.
  - A exclusão não deve apagar os dados do paciente, mas torná-lo como "inativo" no sistema.
  - O horário de funcionamento da clínica é de segunda a sábado, das 07:00 às 19:00;
  - As consultas tem duração fixa de 1 hora;
  - As consultas devem ser agendadas com antecedência mínima de 30 minutos;
  - Não permitir o agendamento de consultas com pacientes inativos no sistema;
  - Não permitir o agendamento de consultas com médicos inativos no sistema;
  - Não permitir o agendamento de mais de uma consulta no mesmo dia para um mesmo paciente;
  - Não permitir o agendamento de uma consulta com um médico que já possui outra consulta agendada na mesma data/hora;
  - A escolha do médico é opcional, sendo que nesse caso o sistema deve escolher aleatoriamente algum médico disponível na data/hora preenchida.
  - É obrigatório informar o motivo do cancelamento da consulta, dentre as opções: paciente desistiu, médico cancelou ou outros;
  - Uma consulta somente poderá ser cancelada com antecedência mínima de 24 horas.

## Tecnologias Utilizadas
- Spring Boot 3: Framework principal para construção da API;
- Java 21: Última versão LTS (Suporte de Longo Prazo) do Java;
- Lombok: Redução de código repetitivo com anotações para geração de getters, setters, toString, entre outros;
- MySQL: Banco de dados relacional para armazenamento de informações;
- Flyway: Controle de versionamento e migração do banco de dados;
- JPA/Hibernate: Persistência de dados com suporte a ORM (Mapeamento Objeto-Relacional);
- Maven: Gerenciamento de dependências e build do projeto;
- Insomnia: Ferramenta para testar requisições da API.
