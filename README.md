<h1 align="center">💼 Desafio Técnico – PicPay</h1>

<p align="center">
  Solução bancária digital integrando com a API oficial do PicPay. Oferece funcionalidades completas <br />
  de carteira digital, pagamentos e transferências de forma segura, escalável e eficiente.
</p>

<div align="center">
  <img src="https://img.shields.io/github/stars/carlos0ff/picpay-digital-wallet?style=for-the-badge&color=yellow" alt="Stars">
  <img src="https://img.shields.io/github/forks/carlos0ff/picpay-digital-wallet?style=for-the-badge&color=blue" alt="Forks">
  <img src="https://img.shields.io/github/issues/carlos0ff/picpay-digital-wallet?style=for-the-badge&color=green" alt="Issues">
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge&logo=open-source-initiative" alt="License">
  <img src="https://img.shields.io/badge/Java-17+-orange?style=for-the-badge&logo=openjdk" alt="Java Version">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version">
</div>

---

---

## 📋 Sumário

- [Sobre o Projeto](#sobre-o-projeto)
- [Arquitetura do projeto](#arquitetura-do-projeto)
- [Contribuição](#contribuição)
- [Licença](#licença)

---

## Sobre o Projeto
Este projeto foi desenvolvido como parte de um [desafio técnico proposto pela PicPay](https://github.com/carlos0ff/picpay-digital-wallet/docs). A aplicação simula uma carteira digital com funcionalidades de:

- Cadastro e autenticação de usuários;
- Realização de transferências entre carteiras;
- Integração com a API oficial do PicPay.

<p>O foco principal está na construção de uma solução segura, escalável e de fácil manutenção, seguindo boas práticas de arquitetura e desenvolvimento backend.</p>

---

## Arquitetura do Projeto

```bash
picpay-digital-wallet/
├── src/
│   ├── main/
│   │   ├── java/com/picpay/
│   │   │   ├── config/        # Configurações da aplicação
│   │   │   │   ├── SwaggerConfig.java   # Documentação API
│   │   │   │   ├── SecurityConfig.java  # Autenticação/autorização
│   │   │   │   └── DatabaseConfig.java  # Configuração do banco
│   │   │   ├── controller/    # Camada de API REST
│   │   │   │   ├── UserController.java       # Gestão de usuários
│   │   │   │   ├── TransactionController.java # Operações financeiras
│   │   │   │   └── AccountController.java    # Consultas de conta
│   │   │   ├── dto/           # Objetos de Transferência de Dados
│   │   │   │   ├── requests/   # DTOs de entrada
│   │   │   │   └── responses/  # DTOs de saída
│   │   │   ├── exception/     # Tratamento de erros
│   │   │   │   ├── GlobalExceptionHandler.java # @ControllerAdvice
│   │   │   │   └── BusinessException.java     # Exceções customizadas
│   │   │   ├── model/         # Entidades de domínio
│   │   │   │   ├── User.java          # Entidade usuário
│   │   │   │   ├── Transaction.java   # Entidade transação
│   │   │   │   └── Account.java       # Entidade conta
│   │   │   ├── repository/    # Camada de acesso a dados
│   │   │   │   ├── UserRepository.java        # Spring Data JPA
│   │   │   │   └── TransactionRepository.java # Spring Data JPA
│   │   │   ├── service/       # Lógica de negócio
│   │   │   │   ├── UserService.java          # Serviços de usuário
│   │   │   │   ├── TransactionService.java   # Serviços financeiros
│   │   │   │   └── NotificationService.java  # Serviço de notificação
│   │   │   └── util/          # Utilitários
│   │   │       ├── CpfValidator.java    # Validador de CPF
│   │   │       └── MoneyUtils.java      # Operações monetárias
│   │   └── resources/
│   │       ├── application.yml          # Configurações principais
│   │       ├── application-dev.yml      # Config para desenvolvimento
│   │       ├── application-prod.yml     # Config para produção
│   │       └── db/
│   │           ├── migration/           # Flyway migrations
│   │           └── data.sql             # Dados iniciais
│   └── test/
│       └── java/com/picpay/
│           ├── unit/            # Testes unitários
│           │   ├── service/     # Testes de serviços
│           │   └── util/        # Testes de utilitários
│           └── integration/     # Testes de integração
│               ├── controller/  # Testes de endpoints
│               └── repository/  # Testes de repositórios
├── Dockerfile                   # Configuração para containerização
├── docker-compose.yml           # Orquestração de containers
├── pom.xml                      # Dependências Maven
├── README.md                    # Documentação principal
└── LICENSE                      # Licença MIT
```
---

## Contribuiçãos

Contribuições são muito bem-vindas! Para colaborar:

1. Faça um fork do repositório
2. Crie uma branch com sua funcionalidade:
   ```bash
   git checkout -b feature/minha-funcionalidade
   ```
3. Faça o commit das suas alterações:
   ```bash
   git commit -m 'Adiciona nova funcionalidade'
   ```
4. Envie para seu fork:
   ```bash
   git push origin feature/minha-funcionalidade
   ```
5. Abra um **Pull Request**

---

## Licença

Este projeto está licenciado sob a licença **MIT**. Consulte o arquivo [LICENSE](LICENSE) para mais informações.

---

<p align="center">
  Desenvolvido com 💚 por <a href="https://github.com/carlos0ff" target="_blank"><strong>José Carlos</strong></a>
</p>