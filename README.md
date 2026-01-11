# 🤖 Bot de Monitoramento Financeiro com n8n

Este projeto é um pipeline de dados automatizado (ETL) construído com **n8n** e **JavaScript**. Ele monitora cotações de ativos financeiros (Criptomoedas e Moedas FIAT) e envia relatórios formatados via Telegram.

<img width="822" height="177" alt="image" src="https://github.com/user-attachments/assets/65617160-cb0e-400c-b62d-dda7412933e1" />


## 🚀 Funcionalidades

- **Extração:** Coleta dados em tempo real via API (CoinGecko / HG Brasil).
- **Transformação:** Processa o JSON bruto utilizando JavaScript para:
  - Formatação monetária (BRL).
  - Cálculo de variação e inserção de emojis (🟢/🔴).
- **Carga/Notificação:** Envia alertas formatados em Markdown para um bot do Telegram.
- **Agendamento:** Execução automática em horários definidos (07:00 e 21:00).

## 🛠️ Tecnologias Utilizadas

- [n8n](https://n8n.io/) - Orquestração de workflow.
- **JavaScript** - Lógica de manipulação de dados.
- **APIs REST** - Integração de sistemas.

## 📦 Como usar este workflow

### Pré-requisitos
1. Uma instância do n8n instalada (local ou nuvem).
2. Um Bot criado no Telegram (via @BotFather).
3. Chave de API da Coingecko.

### Instalação
1. Baixe o arquivo `workflow.json` deste repositório.
2. No n8n, vá em **Menu > Import from File** e selecione o arquivo.
3. Configure suas credenciais:
   - No nó **Telegram**: Adicione seu Token.
   - No nó **HTTP Request**: Insira sua API Key (se necessário).
   - Nos campos de Chat ID: Insira seu ID do Telegram.
