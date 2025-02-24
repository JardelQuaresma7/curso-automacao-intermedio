# Curso de Automação Intermediário com Cypress

Este repositório contém os exercícios e projetos desenvolvidos no **curso intermediário de automação de testes com Cypress**, dando continuidade ao aprendizado iniciado no curso básico. O foco deste módulo foi aprofundar o uso do Cypress, explorando práticas avançadas de testes e integração com diferentes ferramentas.

## 🚀 Tecnologias Utilizadas

- [Cypress](https://www.cypress.io/) - Framework de testes end-to-end
- [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript) - Linguagem utilizada nos testes
- [Node.js](https://nodejs.org/) - Ambiente de execução
- [Mochawesome](https://www.npmjs.com/package/mochawesome) - Relatórios detalhados de testes
- [Cypress Dashboard](https://www.cypress.io/dashboard/) - Monitoramento e execução na nuvem

## 📂 Estrutura do Projeto

```
curso-automacao-intermedio/
├── cypress/
│   ├── e2e/
│   │   ├── login.spec.js
│   │   ├── carrinho.spec.js
│   │   ├── api.spec.js
│   ├── support/
│   ├── fixtures/
├── reports/
├── cypress.config.js
├── package.json
├── README.md
```

- `cypress/e2e/`: Testes automatizados.
- `cypress/support/`: Configurações e funções auxiliares.
- `cypress/fixtures/`: Dados para os testes.
- `reports/`: Relatórios gerados com Mochawesome.

## 🛠️ Configuração do Ambiente

### Pré-requisitos

Antes de executar os testes, instale:

- [Node.js](https://nodejs.org/) (versão 12 ou superior)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)

### Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/JardelQuaresma7/curso-automacao-intermedio.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd curso-automacao-intermedio
   ```

3. Instale as dependências:

   ```bash
   npm install
   ```

   ou

   ```bash
   yarn install
   ```

## ▶️ Executando os Testes

### Executando testes interativos

```bash
npx cypress open
```

ou

```bash
yarn run cypress open
```

### Executando testes no modo headless

```bash
npx cypress run
```

ou

```bash
yarn run cypress run
```

### Gerando relatórios de testes

```bash
npx cypress run --reporter mochawesome
```

## 📌 Exemplo de Teste Avançado

Exemplo de um teste de integração com API:

```javascript
describe('Teste de API', () => {
  it('Deve validar resposta da API', () => {
    cy.request('GET', 'https://jsonplaceholder.typicode.com/posts/1')
      .should((response) => {
        expect(response.status).to.eq(200);
        expect(response.body).to.have.property('id', 1);
      });
  });
});
```

## 🤝 Contribuição

1. Faça um fork do repositório.
2. Crie uma branch (`git checkout -b feature/nova-feature`).
3. Faça commit das mudanças (`git commit -m 'Nova funcionalidade'`).
4. Faça push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

## 📜 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](./LICENSE) para mais detalhes.
