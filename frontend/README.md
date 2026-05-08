# Frontend do Organiza$

## Descrição
O frontend do sistema Organiza$ é a interface do usuário, desenvolvida para ser intuitiva e responsiva, permitindo que os usuários interajam com o sistema de gestão financeira pessoal. Ele consome a API RESTful fornecida pelo backend para exibir dados e gerenciar as operações do usuário.

## Tecnologias
- **React**: Biblioteca JavaScript para construção de interfaces de usuário.
- **TypeScript**: Superset do JavaScript que adiciona tipagem estática, melhorando a robustez e manutenibilidade do código.
- **Vite**: Ferramenta de build de próxima geração que oferece um ambiente de desenvolvimento frontend extremamente rápido.
- **TailwindCSS**: Framework CSS utilitário que permite a construção rápida de designs personalizados diretamente no HTML.

## Estrutura do Projeto
```text
src/
├── core/                        # Configuração de API, Contexto de Autenticação e Temas
│   ├── api/                     # Configurações e clientes da API
│   ├── auth/                    # Lógica de autenticação e gerenciamento de sessão
│   └── theme/                   # Definições de tema e estilos globais
├── features/                    # Módulos baseados em domínio (Auth, Tasks, Projects, etc.)
│   ├── auth/                    # Componentes e lógica relacionados à autenticação
│   ├── tasks/                   # Componentes e lógica relacionados a tarefas/finanças
│   └── projects/                # Componentes e lógica relacionados a projetos
├── components/                  # Componentes de UI reutilizáveis (botões, inputs, modais, etc.)
├── layouts/                     # Templates de layout de página (cabeçalho, rodapé, navegação)
├── hooks/                       # Hooks personalizados do React para lógica reutilizável
├── utils/                       # Funções utilitárias e helpers
└── assets/                      # Imagens, ícones e outros recursos estáticos
```

## Como Executar o Frontend
1.  **Pré-requisitos**: Certifique-se de ter o **Node.js** (versão 18 ou superior) e o **npm** (ou yarn/pnpm) instalados em sua máquina.
2.  **Instalar Dependências**: Navegue até o diretório raiz do frontend (`/home/ubuntu/projeto_organiza/frontend/`) e execute:
    ```bash
    npm install
    # ou yarn install
    # ou pnpm install
    ```
3.  **Iniciar o Servidor de Desenvolvimento**: Após a instalação das dependências, inicie o servidor de desenvolvimento:
    ```bash
    npm run dev
    # ou yarn dev
    # ou pnpm dev
    ```
    O frontend estará acessível em `http://localhost:5173` (porta padrão do Vite, pode variar).

## Variáveis de Ambiente
As variáveis de ambiente necessárias para o frontend estão centralizadas no arquivo `.env.example` na raiz do projeto. Certifique-se de criar um arquivo `.env` baseado nesse modelo.

## Arquitetura
O frontend adota uma arquitetura baseada em componentes, seguindo os princípios do React. As principais decisões arquiteturais incluem:
-   **Componentização**: Interface construída a partir de componentes reutilizáveis e isolados.
-   **Gerenciamento de Estado**: Utilização de Context API ou bibliotecas como Redux/Zustand (se necessário) para gerenciamento de estado global.
-   **Roteamento**: Gerenciado por React Router para navegação entre as páginas.
-   **Tipagem Estática**: Uso de TypeScript para garantir a segurança do tipo e melhorar a qualidade do código.
-   **Design System**: Utilização de TailwindCSS para um design consistente e desenvolvimento ágil da UI.
