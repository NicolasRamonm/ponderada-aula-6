# Smart City - Semáforo Inteligente

Imagine uma cidade onde os semáforos não apenas controlam o tráfego, mas também se comunicam entre si, ajustando o fluxo de veículos de forma inteligente e eficiente. Este projeto tem como objetivo criar um sistema de semáforos inteligentes, que utilizam sensores de luz (LDR) para detectar a presença de veículos e adaptar o comportamento de acordo com diferentes condições, como o modo noturno.

## 📑 Sumário
1. [Descrição do Projeto](#descrição-do-projeto)
2. [Bill of Materials](#bill-of-materials)
3. [Montagem Física e Programação](#montagem-física-e-programação)
4. [Configuração da Interface Online](#configuração-da-interface-online)
5. [Conexão MQTT e Dashboard Ubidots](#conexão-mqtt-e-dashboard-ubidots)
6. [Código](#código)
7. [Demonstração em Vídeo](#demonstração-em-vídeo)
8. [Como Executar o Projeto](#como-executar-o-projeto)

---

## Descrição do Projeto
Este projeto simula semáforos inteligentes em uma cidade. Usando sensores de luz (LDR), o sistema detecta a presença de veículos e adapta seu comportamento para otimizar o tráfego. Durante condições de baixa luminosidade, o sistema entra em modo noturno.

## Bill of Materials
- 2 x Semáforo (com LEDs vermelhos, amarelos e verdes)
- 2 x Sensor LDR
- 2 x Resistor de 10kΩ para o LDR
- 2 x ESP32
- Protoboard e jumpers
- Conexão Wi-Fi
- Conta no Ubidots para monitoramento (opcional)

## Montagem Física e Programação
### Parte 1: Montagem Física
- Monte os semáforos e conecte cada sensor LDR aos pinos analógicos do ESP32.
- Configure o LDR para detectar variação de luz e adaptar o comportamento do semáforo conforme o modo noturno.

### Parte 2: Programação
- Programe o ESP32 para detectar mudanças de luminosidade via LDR e mudar o estado dos LEDs do semáforo.
- Implemente o modo noturno, onde o semáforo opera com luzes intermitentes durante períodos de baixa luminosidade.

## Configuração da Interface Online
Desenvolva uma interface online simples e funcional que permita:
- Ajustar o comportamento dos semáforos
- Ativar ou desativar o modo noturno manualmente
- Visualizar os dados captados pelo LDR em tempo real

## Conexão MQTT e Dashboard Ubidots
- Configure cada ESP32 para enviar dados ao Ubidots via MQTT.
- Crie um dashboard no Ubidots para monitoramento centralizado dos semáforos e ajuste de parâmetros do sistema em tempo real.
- Configure o MQTT para sincronizar ambos os semáforos, permitindo comunicação eficiente entre eles.

## Código
Inclua o código completo do projeto, separado em seções para facilitar a leitura e compreensão:
- **Configuração do LDR e detecção de veículos**
- **Modo noturno**
- **Conexão MQTT para Ubidots**

```c++
// Exemplo de trecho de código
#include <WiFi.h>
#include <Ubidots.h>
// Configuração de pinos, LDR e lógica do semáforo
