# 📋 Milky Flow Board Service

O Milky Flow Board Service é um microserviço especializado no gerenciamento eficiente dos quadros no aplicativo Milky Flow. Ele oferece uma infraestrutura robusta para criar, organizar e rastrear os quadros, proporcionando aos usuários controle total sobre seus projetos.

## 🛠️ Tecnologias Utilizadas

- Linguagem de Programação: Java
- Framework: Spring Boot
- Banco de Dados: MongoDB
- Mensageria: RabbitMQ

## 🚀 Funcionalidades

- Criação de Quadros
- Atualização de Quadros
- Exclusão de Quadros
- Associação de Usuários aos Quadros
- Consulta de Quadros por ID
- Publicação de Eventos de Quadros (RabbitMQ)

## ✅ Pré-requisitos

Antes de iniciar, certifique-se de ter as seguintes ferramentas instaladas:

- Java Development Kit (JDK) 8 ou superior
- Docker (para configurar o ambiente com Docker Compose)

## 📦 Instalação

1. Clone este repositório para sua máquina local.
2. Execute `mvn clean install` para instalar as dependências.
3. Configure as propriedades do MongoDB em `src/main/resources/application.properties`.
4. Configure o RabbitMQ em `src/main/resources/application.properties`.
5. Configure o banco de dados MongoDB com Docker Compose:
    - Abra um terminal na pasta raiz do projeto e execute:
      ```sh
      docker-compose up -d
      ```
6. Execute `./mvnw spring-boot:run` para iniciar o microserviço.

## 🌐 Endpoints

- `GET /boards` - Listar todos os quadros.
- `GET /boards/{boardId}` - Obter detalhes de um quadro específico.
- `POST /boards` - Criar um novo quadro.
- `PUT /boards/{boardId}` - Atualizar um quadro existente.
- `DELETE /boards/{boardId}` - Excluir um quadro.
- `POST /boards/{boardId}/users` - Associar um usuário a um quadro.

## 📡 Eventos de Quadros (RabbitMQ)

- `BoardCreatedEvent` - Emitido quando um novo quadro é criado.
- `BoardUpdatedEvent` - Emitido quando as informações de um quadro são atualizadas.
- `BoardDeletedEvent` - Emitido quando um quadro é excluído.
- `UserAssignedToBoardEvent` - Emitido quando um usuário é associado a um quadro.

## 🔒 Segurança

Este microserviço implementa medidas de segurança para proteger os dados dos quadros.

## 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests.

## 📄 Licença

Este projeto está licenciado sob a [licença MIT](LICENSE).
