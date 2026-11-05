# Sistema de Recomendacoes de Compras

Aplicacao web demonstrativa de um e-commerce, criada para explorar uma interface de recomendacoes e o uso de machine learning no navegador.

## Funcionalidades atuais

- Carrega produtos e usuarios dos arquivos JSON em `data/`.
- Exibe produtos, perfil do usuario selecionado e historico de compras.
- Guarda os usuarios da sessao em `sessionStorage`.
- Envia eventos de treinamento para um Web Worker e mostra o progresso na interface.

> **Estado do modelo:** o treinamento no Web Worker ainda e uma simulacao de progresso. A funcao de recomendacao esta em desenvolvimento e ainda nao retorna recomendacoes calculadas por um modelo.

## Tecnologias

- JavaScript com ES modules
- BrowserSync para servir a aplicacao localmente e observar alteracoes
- Bootstrap e Bootstrap Icons
- TensorFlow.js e TensorFlow.js Vis carregados por CDN
- Web Worker para o fluxo de treinamento

## Requisitos

- Node.js e npm
- Conexao com a internet para carregar as bibliotecas servidas por CDN

## Como executar

Na pasta do projeto, instale as dependencias e inicie o servidor:

```bash
npm install
npm start
```

Abra [http://localhost:3000](http://localhost:3000) no navegador. O BrowserSync atualiza a pagina quando os arquivos monitorados mudam.

## Estrutura do projeto

```text
data/          Dados de produtos e usuarios
src/controller Controladores da interface, eventos e worker
src/events/    Eventos compartilhados pela aplicacao
src/service/   Carregamento e persistencia dos dados
src/view/      Views e templates HTML
src/workers/   Web Worker do treinamento e recomendacoes
index.html     Pagina principal
style.css      Estilos da aplicacao
```

## Scripts npm

- `npm start`: inicia o BrowserSync na porta 3000.
- `npm test`: ainda nao esta configurado.

## Licenca

Este projeto esta disponivel sob a licenca MIT. Consulte [LICENSE](LICENSE).