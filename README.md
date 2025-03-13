# Portfólio técnico

Este é um projeto de testes automatizados utilizando Postman para escrita dos testes e rodando com Newman.

Estrutura do Projeto</br>
ReqRes.postman_collection.json coleção com as requisições e testes escritos em JavaScript.</br>


Neste demostrativo realizo testes funcionais de criação de usuários e login da API pública https://reqres.in/.</br>
Swagger https://reqres.in/api-docs/#/

Lembrando que é uma amostra de como eu estruturo os testes e quais métodos utilizo!

## Configuração do workflow

```bash

Executa automaticamente os testes sempre que houver um push ou pull request na main.
Permite rodar manualmente pelo GitHub Actions (workflow_dispatch).
Instala o Node.js e o Newman no ambiente do GitHub Actions.
Executa os testes com a collection ReqProd.postman_environment.json e o ambiente ReqProd.postman_environment.json.
Gera um relatório HTML e o salva nos artefatos do workflow.

```

## Execução local

Instalação do Newman

```bash
npm install -g newman

```

Rodando os testes localmente via Newman:

```bash
newman run ReqRes.postman_collection.json
```

Rodando os testes e gerando relatórios de execução:

```bash
newman run ReqRes.postman_collection.json.json -r html,cli --reporter-html-export report.html

```
