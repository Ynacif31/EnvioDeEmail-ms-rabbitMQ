# Envio de E-mail Microserviço com RabbitMQ

Este projeto é um microserviço desenvolvido em **Java** utilizando **Spring Boot**, que realiza o envio de e-mails de forma assíncrona, integrando-se ao **RabbitMQ** para gerenciamento de filas.

---

## 📋 Funcionalidades

- Envio de e-mails de forma assíncrona.
- Integração com RabbitMQ para comunicação via mensageria.
- Logs detalhados para monitoramento das operações.

---

## 📂 Estrutura do Projeto

- **controller**: Contém os endpoints REST para interação com o serviço.
- **service**: Implementa a lógica de envio de e-mails.
- **model**: Define as classes de domínio e DTOs.
- **config**: Configurações para integração com RabbitMQ.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Java
- **Framework:** Spring Boot
- **Mensageria:** RabbitMQ
- **Dependências:**
  - spring-boot-starter-web
  - spring-boot-starter-amqp
  - spring-boot-starter-mail
  - spring-boot-starter-data-jpa
  - spring-boot-starter-test

---

## 🚀 Como Executar

### **Pré-requisitos**

Certifique-se de ter instalado:
- Java 17 ou superior
- Maven 3.9.9 ou superior
- RabbitMQ configurado e em execução
- Banco de dados (dependendo da configuração do projeto)

### **Passos para execução**

1. Clone o repositório:
   ```git clone https://github.com/Ynacif31/EnvioDeEmail-ms-rabbitMQ.git```
   ```cd EnvioDeEmail-ms-rabbitMQ ```
### **Configure o RabbitMQ e o serviço de e-mail no arquivo application.properties:**

```
spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
spring.rabbitmq.username=guest
spring.rabbitmq.password=guest
spring.mail.host=smtp.seuprovedor.com
spring.mail.port=587
spring.mail.username=seu-email@provedor.com
spring.mail.password=sua-senha
```
### **Compile e execute o projeto**
```
mvn spring-boot:run
```
# Endpoints Disponíveis

### Enviar E-mail

**POST /send-email**  
- **Descrição:** Envia um e-mail baseado nos dados fornecidos no corpo da requisição.  
- **Body:**  
  ```
  json
  {
    "to": "destinatario@exemplo.com",
    "subject": "Assunto do e-mail",
    "body": "Conteúdo do e-mail"
  }
  
### **Melhorias Futuras**
	•	Implementar sistema de retries para falhas no envio de e-mails.
	•	Monitoramento das filas no RabbitMQ.
	•	Desenvolver um painel administrativo para gerenciar e-mails.




  
