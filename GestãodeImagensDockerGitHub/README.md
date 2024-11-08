# Automação de Build e Deploy com Docker e GitHub Actions

Este repositório contém a automação de build, testes e deploy de uma aplicação web moderna composta por três componentes principais:

1. **Front-End**: Construído com React.
2. **Back-End**: Construído com Node.js e Express.
3. **Banco de Dados**: Utiliza PostgreSQL.

## Estrutura do Repositório

- `frontend/`: Contém o Dockerfile e o código da aplicação React.
- `backend/`: Contém o Dockerfile e o código da API Node.js + Express.
- `database/`: Contém o Dockerfile para configurar o PostgreSQL.

## Workflow de GitHub Actions

Este repositório possui dois workflows principais no GitHub Actions:

1. **Build and Test**: Constrói as imagens Docker de cada componente, executa os testes e garante que os contêineres estão funcionando corretamente.
2. **Deploy**: Publica as imagens Docker no Docker Hub e simula um deploy para um ambiente de produção.

## Como Funciona

- Ao fazer push ou pull request para a branch `main`, o workflow de **Build and Test** é executado, criando e testando as imagens Docker para cada componente.
- Quando a branch `main` é atualizada com sucesso, o workflow de **Deploy** é acionado para enviar as imagens para o Docker Hub e simular o deploy para o ambiente de produção.

## Requisitos

- Conta no Docker Hub (para publicar as imagens).
- GitHub Secrets configurados com seu Docker Hub Username e Password.

## Como Usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/usuario/repositorio.git
