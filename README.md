# Banco Web Tests

Automação de testes end-to-end para a aplicação Banco Web utilizando Cypress e JavaScript.

## Objetivo

Garantir a qualidade das principais funcionalidades da aplicação Banco Web por meio de testes automatizados.

## Componentes do Projeto

- **Cypress:** Framework de testes end-to-end.
- **Custom Commands:** Comandos personalizados para facilitar ações recorrentes nos testes, localizados em `cypress/support/commands.js`.
- **cypress-mochawesome-reporter:** Geração de relatórios detalhados dos testes (adicionar ao projeto se necessário).
- **package.json:** Gerenciamento das dependências e scripts do projeto.
- **cypress.config.js:** Configuração principal do Cypress, incluindo o endereço base da aplicação.

## Estrutura de Pastas

- `cypress/integration/` — Testes automatizados.
- `cypress/support/commands.js` — Custom Commands.
- `reports/` — Relatórios gerados após a execução dos testes.
- `cypress.config.js` — Configuração do Cypress.

## Pré-requisitos

- Node.js instalado
- npm instalado
- **Importante:** A API (`banco-api`) e a aplicação Web (`banco-web`) devem estar em execução antes de rodar os testes.

## Instalação

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```

## Execução dos Testes

1. Certifique-se de que a API e a aplicação Web estão rodando.
2. Execute os testes em modo headless:
   ```bash
   npm test
   ```
3. Execute os testes com interface gráfica:
   ```bash
   npm run cy:open
   ```
4. Execute os testes em modo headed:
   ```bash
   npm run cy:headed
   ```
5. Para gerar relatórios com Mochawesome (se instalado):
   ```bash
   npx cypress run --reporter mochawesome
   ```

## Documentação dos Testes

Os testes cobrem cenários como:

- Login
- Cadastro de usuários
- Transações bancárias
- Validação de campos obrigatórios

## Custom Commands

Os Custom Commands estão definidos em `cypress/support/commands.js` e incluem funções para:

- Realizar login
- Preencher formulários
- Validar mensagens de erro
- Executar ações repetitivas de forma simplificada

## Relatórios

Após a execução dos testes, os relatórios detalhados podem ser encontrados na pasta `reports/`, facilitando a análise dos resultados.

---

Contribuições são bem-vindas! 
