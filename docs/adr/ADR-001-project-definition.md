# ADR-001 — Definição do Projeto

## Status
Definido

## Contexto
O projeto Organiza$ nasceu da necessidade de um sistema de organização financeira pessoal eficiente, que ofereça controle total sobre receitas, despesas e a saúde financeira mensal. Além de ser uma ferramenta prática para o dia a dia, o projeto tem como objetivo servir como um laboratório para a aplicação de padrões avançados de engenharia de software, arquitetura moderna e boas práticas de desenvolvimento.

## Decisão
O Organiza$ será desenvolvido como uma aplicação fullstack moderna, adotando uma arquitetura de **Monolito Modular** no backend para separar a infraestrutura técnica dos domínios de negócio, facilitando uma futura migração para microsserviços, se necessário.

As tecnologias escolhidas são:
- **Backend**: Java 21 com Spring Boot 3. A escolha se deve à robustez do ecossistema Spring para aplicações corporativas. A API será RESTful.
- **Segurança**: Spring Security com JWT (JSON Web Token) para autenticação stateless, garantindo escalabilidade.
- **Persistência**: Spring Data JPA e Hibernate, com banco de dados MySQL 8.0+.
- **Migrações de Banco de Dados**: Flyway, para garantir o controle de versão do esquema do banco de dados de forma automatizada e confiável.
- **Frontend**: React com TypeScript, utilizando Vite como bundler para otimização do build e TailwindCSS para estilização rápida e responsiva.

## Consequências
- **Positivas**:
  - Estrutura profissional que favorece o aprendizado técnico e a aplicação de boas práticas (Clean Code, SOLID).
  - Alta manutenibilidade e escalabilidade devido à arquitetura modular e autenticação stateless.
  - Controle rigoroso sobre as mudanças no banco de dados através do Flyway.
- **Negativas**:
  - Aumento da complexidade inicial do projeto devido às decisões arquiteturais (Monolito Modular vs. Monolito Tradicional).
  - Curva de aprendizado maior para novos desenvolvedores que não estejam familiarizados com todas as tecnologias da stack.
