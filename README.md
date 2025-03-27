# Projeto de Bot do Telegram com Flask e Thinger.io

Este projeto consiste em um bot do Telegram integrado a uma API Flask e ao Thinger.io, com o objetivo de gerenciar e monitorar dados de consumo de energia elétrica. Ele permite a comunicação entre diferentes componentes para fornecer informações úteis, como consumo atual, total e estimativa de custo.

---

## Índice

1. [Descrição do Projeto](#descrição-do-projeto)  
2. [Funcionalidades](#funcionalidades)  
3. [Configuração e Instalação](#configuração-e-instalação)  
   - [Configuração dos Tokens e Credenciais](#configuração-dos-tokens-e-credenciais)  
4. [Como Utilizar](#como-utilizar) 
---

## Descrição do Projeto

Este projeto tem como finalidade facilitar o monitoramento e gerenciamento de energia elétrica utilizando os dados vindos do sensor SCT-013 com a placa Raspberry Pi Pico W conectada à internet (IoT), por meio de um computador de borda conectado ao Thinger.io. Ele também utiliza um bot Telegram para criar uma interface interativa para os usuários.

O fluxo principal inclui:
- Flask para lidar com requisições HTTP.
- O Thinger.io como plataforma de IoT.
- Um bot Telegram que exibe os dados processados em um menu interativo.

---

## Funcionalidades

- **Atualização de Dados**: Os dados de potência (kW), consumo total (kWh) e estimativa de custo são atualizados via requisições HTTP e enviados ao Thinger.io.
- **Menu no Bot Telegram**:
  - Consumo Atual em tempo real.
  - Consumo Total acumulado.
  - Estimativa de custo em reais.
  - Link para dashboard gráfico no Thinger.io.
- **Infraestrutura Multithread**: O bot Telegram e o servidor Flask rodam em threads separadas para maior eficiência.
  - O servidor Flask e o bot do Telegram são executados simultaneamente em threads separadas, permitindo a interação contínua enquanto o servidor Flask coleta e envia os dados. 

## Configuração e Instalação

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/antoniojosemota/servidor_SMILE.git
  
## Configuração dos Tokens e Credenciais

### Telegram Bot Token
Substitua `BOT_TOKEN` pelo token do seu bot do Telegram (obtido via [@BotFather](https://t.me/BotFather)):

```python
Token do chat telegram
BOT_TOKEN = 'SEU_TOKEN'

Credenciais do dispositivo Thinger.io
THINGER_USERNAME = 'USERNAME'
THINGER_DEVICE_ID = 'DEVICE_ID'
THINGER_DEVICE_CREDENTIAL = 'DEVICE_CREDENCIAL'

ID do chat do Telegram
TELEGRAM_CHAT_ID = 'SEU_CHAT_ID
```

## Como Utilizar

### Como Executar o Script Principal

Para iniciar o sistema, execute o arquivo Python principal com o comando:

```bash
python3 nome_do_arquivo.py

Após iniciar, ira se conectar ao Thinger IO e vai ativar o bot no Telegram.
