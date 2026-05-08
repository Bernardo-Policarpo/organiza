# Backend do Organiza$

## Descrição
O backend do sistema Organiza$ é responsável por toda a lógica de negócio, persistência de dados e exposição de uma API RESTful para o frontend. Ele foi projetado com uma arquitetura de Monolito Modular, visando alta coesão, baixo acoplamento e facilidade de manutenção e escalabilidade.

## Tecnologias
- **Java 21** & **Spring Boot 3**: Framework principal para desenvolvimento da aplicação.
- **Spring Security** com **JWT**: Para autenticação e autorização seguras e stateless.
- **Spring Data JPA** & **Hibernate**: Para persistência de dados e interação com o banco de dados.
- **MySQL**: Banco de dados relacional utilizado para armazenar as informações do sistema.
- **Flyway**: Ferramenta para controle de versão e migrações do esquema do banco de dados.
- **Lombok**: Biblioteca para reduzir o código boilerplate em classes Java.
- **Maven**: Ferramenta para gerenciamento de dependências e construção do projeto.

## Estrutura do Projeto
```text
src/main/java/com/organiza/backend/
├── core/                        # Infraestrutura e Configurações Globais
│   ├── config/                  # Beans de Configuração
│   ├── security/                # Implementação de Segurança e JWT
│   ├── exception/               # Tratamento Global de Exceções
│   └── response/                # Respostas Padronizadas da API
├── modules/                     # Módulos de Domínio de Negócio
│   ├── auth/                    # Lógica de Autenticação
│   ├── users/                   # Gestão de Usuários
│   ├── tasks/                   # Controle de Tarefas/Financeiro
│   └── projects/                # Organização de Projetos
└── shared/                      # Componentes Reutilizáveis
```

## Como Executar o Backend
1.  **Pré-requisitos**: Certifique-se de ter o **Java 21** e o **Maven** instalados em sua máquina.
2.  **Configuração do Banco de Dados**: Configure suas credenciais do MySQL no arquivo `src/main/resources/application.properties` ou através das variáveis de ambiente detalhadas no arquivo `.env.example` na raiz do projeto.
3.  **Executar**: Navegue até o diretório raiz do backend (`/home/ubuntu/projeto_organiza/backend/`) e execute o seguinte comando:
    ```bash
    mvn spring-boot:run
    ```
    O backend estará disponível em `http://localhost:8080` (porta padrão do Spring Boot).

## Variáveis de Ambiente
As variáveis de ambiente necessárias para o backend estão centralizadas no arquivo `.env.example` na raiz do projeto. Certifique-se de criar um arquivo `.env` baseado nesse modelo.

## Arquitetura
O backend segue uma **Arquitetura Modular Orientada a Domínio**, com as seguintes decisões principais:
-   **Autenticação Stateless**: Utiliza JWT para garantir que as sessões não dependam do estado do servidor, facilitando a escalabilidade.
-   **Tratamento Global de Exceções**: Implementação centralizada para lidar com erros e retornar respostas padronizadas da API.
-   **Migrações de Banco de Dados**: Gerenciadas pelo Flyway, garantindo que o esquema do banco de dados esteja sempre sincronizado com a versão do código.
-   **Padrão DTO (Data Transfer Object)**: Utilizado para desacoplar as entidades de domínio internas dos contratos externos da API, promovendo segurança e flexibilidade.
