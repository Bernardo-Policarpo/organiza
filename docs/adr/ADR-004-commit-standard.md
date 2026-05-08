# ADR-004 — Padronização de Commits

## Status
Definido

## Contexto
O sistema precisa seguir um padrão rígido de commit para facilitar a rastreabilidade, a revisão de código e a geração automática de changelogs. Commits inconsistentes dificultam a leitura do histórico e o entendimento das mudanças.

## Decisão
Será adotado um padrão de commits baseado no Conventional Commits, com tipos e escopos bem definidos, e mensagens claras e concisas. As mensagens de commit devem ser escritas em inglês, ser generalizadas e usar letras minúsculas (exceto siglas e nomes próprios).

### Padrão de Commits
O formato geral do commit deve ser: `tipo(escopo): mensagem`

#### Tipos de Commit (Type)
| Tipo       | Descrição                                                                 |
| :--------- | :------------------------------------------------------------------------ |
| `feat`     | Uma nova funcionalidade ou adição (feature)                               |
| `fix`      | Uma correção de bug                                                       |
| `chore`    | Mudanças na construção, dependências ou ferramentas (sem alteração de código de produção) |
| `docs`     | Alterações apenas na documentação                                         |
| `style`    | Mudanças que não afetam o significado do código (espaços em branco, formatação, ponto e vírgula ausente, etc.) |
| `refactor` | Uma mudança de código que não adiciona uma funcionalidade nem corrige um bug |
| `perf`     | Uma mudança de código que melhora o desempenho                            |
| `test`     | Adição de testes ausentes ou correção de testes existentes                |
| `build`    | Mudanças que afetam o sistema de build ou dependências externas (ex: maven, npm) |
| `ci`       | Mudanças nos arquivos e scripts de configuração de CI                     |
| `revert`   | Reverte um commit anterior                                                |

#### Escopo (Scope)
O escopo é **obrigatório** e deve identificar a área afetada pelo commit. Exemplos de escopos:
`auth`, `appointments`, `users`, `clinics`, `models`, `schemas`, `services`, `api`, `core`, `docker`, `adr-00x`, `readme`, `database`, `frontend`, `backend`.

#### Mensagem (Subject)
A mensagem deve ser uma descrição concisa e imperativa da mudança, com no máximo 72 caracteres. Deve iniciar com letra minúscula e não terminar com ponto.

### Exemplos de Commits
- `feat(appointments): add appointment creation endpoint`
- `fix(auth): correct token expiration validation`
- `docs(adr-006): update package manager from NPM to Bun`
- `chore(docker): add postgres service to compose`
- `refactor(users): improve user service logic`
- `test(api): add unit tests for user API`

### Fluxo de Trabalho (Opcional, mas recomendado)
1.  `git add <arquivos>`
2.  `git commit -m "tipo(escopo): mensagem"`
3.  (Code Review)
4.  Executar formatadores e linters (ex: Black, Ruff para Python; Prettier, ESLint para JS/JSX/HTML).
5.  `git add <arquivos formatados>`
6.  `git commit -m "chore(formatting): apply formatting after review"`

> **Importante**: Formatadores (Black, Ruff, Prettier, ESLint) devem ser executados **após** o code review estar aprovado, não antes. Rodar formatadores antes polui o diff com mudanças puramente estéticas, dificultando a revisão.

## Consequências
- **Histórico limpo e melhor rastreabilidade**: Facilita a navegação e compreensão do histórico do projeto.
- **Geração automática de Changelogs**: Permite a criação automatizada de changelogs a partir dos commits.
- **Melhora na revisão de código**: Diffs mais limpos e focados nas mudanças lógicas.
- **Boas práticas**: Promove a disciplina e a padronização no versionamento.
- **Facilidade na localização e identificação de alterações no repositório**.
