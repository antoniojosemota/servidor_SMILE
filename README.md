# Projeto de Bot do Telegram com Flask e Thinger.io

Este projeto consiste em um bot do Telegram integrado a uma API Flask e ao Thinger.io, com o objetivo de gerenciar e monitorar dados de consumo de energia elétrica. Ele permite a comunicação entre diferentes componentes para fornecer informações úteis, como consumo atual, total e estimativa de custo.

---

## Índice

1. [Descrição do Projeto](#descrição-do-projeto)
2. [Funcionalidades](#funcionalidades)
4. [Configuração e Instalação](#configuração-e-instalação)
5. [Endpoints do Flask](#endpoints-do-flask)
6. [Como Utilizar](#como-utilizar)
7. [Notas de Segurança](#notas-de-segurança)
8. [Licença](#licença)

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

## Configuração e Instalação

1. **Clone o repositório**:
   ```bash
   git clone <(https://github.com/antoniojosemota/servidor_SMILE.git)>
   cd <nome-do-diretorio>
