# Organiza$

## Descrição
O **Organiza$** é um sistema moderno de gestão financeira pessoal, projetado para oferecer controle total sobre receitas, despesas e a saúde financeira mensal. Desenvolvido com foco em arquitetura de alto nível e boas práticas, ele serve tanto como uma ferramenta prática para o dia a dia quanto como um laboratório para padrões avançados de engenharia de software.

## Objetivo
O objetivo principal do Organiza$ é simplificar a organização financeira através de funcionalidades como:
- Controle de receitas e despesas
- Fechamentos financeiros mensais e anuais
- Categorização financeira e histórico de movimentações
- Relatórios detalhados e dashboards interativos

## Tecnologias
Para uma visão detalhada das tecnologias utilizadas em cada parte do projeto, consulte os READMEs específicos:
- [Backend](./backend/README.md)
- [Frontend](./frontend/README.md)
- [Banco de Dados](./database/README.md)

## Estrutura do Projeto
O projeto segue uma arquitetura de **Monolito Modular**, separando a infraestrutura técnica dos domínios de negócio. Para detalhes sobre a estrutura de cada componente principal, consulte:
- [Estrutura do Backend](./backend/README.md#estrutura-do-projeto)
- [Estrutura do Frontend](./frontend/README.md#estrutura-do-projeto)
- [Estrutura do Banco de Dados](./database/README.md#estrutura)

## Como Executar o Projeto
Para instruções detalhadas sobre como configurar e executar cada parte do projeto, consulte os READMEs específicos:
- [Executar o Backend](./backend/README.md#como-executar-o-backend)
- [Executar o Frontend](./frontend/README.md#como-executar-o-frontend)

## Variáveis de Ambiente
As variáveis de ambiente necessárias para o funcionamento do projeto estão detalhadas nos READMEs de cada componente:
- [Variáveis de Ambiente do Backend](./backend/README.md#variáveis-de-ambiente)
- [Variáveis de Ambiente do Frontend](./frontend/README.md#variáveis-de-ambiente)

## Arquitetura
Este projeto implementa uma **Arquitetura Modular Orientada a Domínio**. As decisões arquiteturais e os princípios que guiam o desenvolvimento estão documentados nas ADRs (Architecture Decision Records) e nos READMEs específicos de cada componente.

## Convenções
- **Commits**: Segue o padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/). Mais detalhes em [ADR-004 — Padronização de Commits](./docs/adr/ADR-004-commit-standard.md).
- **Idioma**: Código e documentação são realizados em **Português**, exceto os commits que são feitos em **Inglês**.
- **Estilo de Código**: Princípios de Clean Code e padrões SOLID são aplicados.
- **Padronização de READMEs**: Todos os READMEs seguem o padrão definido em [ADR-002 — Padronização de README](./docs/adr/ADR-002-readme-standard.md).
- **Padronização de ADRs**: As decisões arquiteturais são documentadas conforme [ADR-003 — Padronização de ADRs](./docs/adr/ADR-003-adr-standard.md).

## ADRs (Architecture Decision Records)
Decisões relevantes estão documentadas no diretório `docs/adr/`:
- [ADR-001]: Definição do Projeto
- [ADR-002]: Padronização de README
- [ADR-003]: Padronização de ADR
- [ADR-004]: Padronização de Commits

---
*Desenvolvido para organização pessoal e excelência técnica.*
