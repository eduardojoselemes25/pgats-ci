# Trabalho Final - Integração Contínua de Automação de Testes

## Objetivo

Este projeto foi desenvolvido como trabalho final da disciplina de Integração Contínua da Pós-Graduação em Automação de Testes do Júlio de Lima.

O objetivo é demonstrar a implementação de uma pipeline de Integração Contínua (CI) utilizando GitHub Actions para automatizar a execução dos testes, geração de relatórios e disponibilização dos resultados.

## Conceito de Integração Contínua

Integração Contínua (Continuous Integration - CI) é uma prática de desenvolvimento de software que consiste em executar validações automáticas sempre que alterações são realizadas no código-fonte.

Com essa abordagem é possível identificar problemas rapidamente, aumentar a qualidade do software e reduzir riscos durante o desenvolvimento.

## Tecnologias Utilizadas

- Node.js
- Yarn
- Playwright
- GitHub Actions

## Estrutura da Pipeline

A pipeline foi implementada utilizando GitHub Actions e possui as seguintes etapas:

1. Checkout do código-fonte.
2. Instalação do Node.js.
3. Instalação das dependências do projeto.
4. Instalação dos navegadores necessários para execução do Playwright.
5. Execução dos testes automatizados.
6. Geração dos relatórios de execução.
7. Publicação dos relatórios como Artifacts.

## Gatilhos da Pipeline

### Execução por Push

A pipeline é executada automaticamente sempre que um push é realizado na branch principal do projeto.

### Execução Manual

A execução manual é realizada através do recurso `workflow_dispatch`, disponível na interface do GitHub Actions.

### Execução Agendada

A pipeline também possui execução automática agendada através do recurso `schedule`, utilizando expressões cron.

## Testes Automatizados

Os testes automatizados foram implementados utilizando Playwright.

Para execução local dos testes:

```bash
yarn install

npx playwright install

yarn run e2e
```

## Relatórios

Após a execução dos testes, o Playwright gera relatórios contendo os resultados da execução.

Esses relatórios permitem identificar:

- Testes aprovados.
- Testes reprovados.
- Evidências de execução.
- Detalhes de falhas encontradas.

## Publicação dos Relatórios

Os relatórios são armazenados e publicados como Artifacts do GitHub Actions, permitindo consulta e download diretamente pela interface do GitHub.

## Benefícios da Solução

- Automação da validação do código.
- Execução automática dos testes.
- Histórico das execuções.
- Disponibilização dos relatórios para análise.
- Maior confiabilidade nas entregas.

## Evidências

Para validação do trabalho, deve ser apresentada pelo menos uma execução bem-sucedida da pipeline contendo:

- Status de sucesso da execução.
- Relatório armazenado como Artifact.
- Histórico da execução no GitHub Actions.

## Repositório

https://github.com/eduardojoselemes25/pgats-ci
