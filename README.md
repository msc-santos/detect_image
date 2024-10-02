# API de Reconhecimento de Imagens e Tradução

Este projeto foi desenvolvido utilizando Node.js com o framework Serverless e faz uso dos serviços AWS Rekognition e AWS Translate. Ele permite que você envie uma requisição GET com a URL de uma imagem, reconhece os objetos ou cenas presentes na imagem e traduz o resultado para o português.

## Funcionalidades

- **Reconhecimento de Imagens**: Utiliza o AWS Rekognition para analisar a imagem e detectar objetos, cenas ou textos.
- **Tradução**: Traduz o texto ou rótulos detectados para o português utilizando o AWS Translate.
- **API Simples**: Envie uma requisição GET com o parâmetro de query `imageUrl`, e receba uma descrição da imagem traduzida para o português.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript para código no lado do servidor.
- **Framework Serverless**: Utilizado para implantar e gerenciar funções AWS Lambda.
- **AWS Rekognition**: Serviço usado para análise de imagem e detecção de objetos.
- **AWS Translate**: Serviço de tradução automática de idiomas.
- **Axios**: Cliente HTTP baseado em Promises para fazer requisições.
- **AWS SDK**: Para interagir com os serviços AWS, como Rekognition e Translate.

## Como Funciona

1. **Envio da Requisição**: Faça uma requisição GET para a API, passando a URL de uma imagem como parâmetro de query (exemplo: `?imageUrl=https://exemplo.com/imagem.jpg`).
2. **Reconhecimento de Imagem**: A API utiliza o AWS Rekognition para analisar a imagem e detectar objetos ou cenas.
3. **Tradução**: Os rótulos ou textos detectados são traduzidos para o português usando o AWS Translate.
4. **Resposta**: Um JSON com a descrição traduzida é retornado.

## Exemplo de Uso

```bash
GET /analyse?imageUrl=https://exemplo.com/imagem-exemplo.jpg
```

## Instalação

```bash
git clone https://github.com/msc-santos/detect_image.git
cd detect_image

npm install
```

## Executando Localmente

```bash
serverless offline
```

## Implantação

```bash
serverless deploy
```
