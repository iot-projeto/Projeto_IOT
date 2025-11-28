## Sistema de Alerta para Prevenção de Perdas Particulares em Alagamentos

Este projeto apresenta um sistema IoT completo, capaz de monitorar o nível da água em áreas de risco e emitir alertas preventivos em tempo real via WhatsApp, simulando um dispositivo físico baseado em ESP32 e sensor ultrassônico HC-SR04.
Toda a arquitetura foi desenvolvida e testada em ambiente virtual utilizando Wokwi, Node-RED, MQTT, InfluxDB e Grafana.

## Dashboard
<img width="1476" height="656" alt="image" src="https://github.com/user-attachments/assets/a6c89a24-6e87-43bb-a812-c1ae6b6bb5ea" />

## Link dos dispositivos: 

https://wokwi.com/projects/448738152659097601

https://wokwi.com/projects/446560237280494593

---

Objetivo

Criar uma solução tecnológica de baixo custo e fácil implementação que auxilie na prevenção de danos causados por enchentes e alagamentos, permitindo:

Monitoramento contínuo do nível da água

Detecção automática de situações de risco

Armazenamento e análise histórica dos dados coletados

Emissão de alertas instantâneos ao usuário


O projeto está alinhado aos ODS 11 (Cidades Sustentáveis) e ODS 13 (Ação Climática).


---

Tecnologias Utilizadas

Hardware (simulado no Wokwi)

ESP32

HC-SR04 — Sensor Ultrassônico


Comunicação

MQTT (via Broker no Node-RED)


Backend e Processamento

Node-RED

Recebimento das leituras do sensor

Classificação de risco (Normal / Atenção / Crítico)

Envio de alertas via WhatsApp

Registro das medições no banco de dados



Banco de Dados

InfluxDB

Armazenamento de séries temporais

Consultas históricas via Data Explorer



Visualização

Grafana

Dashboard em tempo real

Histórico das últimas 24h

Gráficos de nível de água e alertas emitidos



Notificações

CallMeBot API — mensagens automáticas no WhatsApp



---

Fluxo Completo da Solução

Wokwi (ESP32 + HC-SR04)
          ↓
        MQTT
          ↓
      Node-RED
   ↓           ↓
InfluxDB   WhatsApp Alertas
          ↓
        Grafana


---

Demonstrações

Simulação do Dispositivo (Wokwi)

Simulação do ESP32 medindo a distância da água.

Node-RED

Fluxo responsável por:

Processar leituras

Identificar risco

Registrar dados

Enviar alertas

InfluxDB

Histórico completo de todas as medições para análises.

Grafana Dashboard

Painel em tempo real mostrando:

Nível da água

Últimas 24h

Total de alertas enviados


WhatsApp

Envio automático de mensagens de alerta conforme nível detectado.


---

Como Executar o Projeto

1. Simulação do ESP32

Abra o código no Wokwi e execute o sensor ultrassônico simulando variação do nível de água.

2. Configure o Node-RED

Importe o fluxo fornecido no repositório
Configure:

Broker MQTT

API de mensagens

Conexão com InfluxDB


3. Configurar Banco de Dados InfluxDB

Crie o bucket

Configure o token de acesso

Conecte ao Node-RED


4. Configurar o Dashboard no Grafana

Importe o dashboard disponibilizado

Conecte à fonte de dados InfluxDB


5. Ativar Alertas via WhatsApp

Gere sua chave no CallMeBot

Configure seu número no fluxo do Node-RED



---

Resultados Obtidos

Tempo médio inferior a 2 segundos entre leitura → processamento → alerta.

Precisão de ~90% para nível de atenção (8–14 cm).

Precisão total para nível crítico (> 15 cm).

Registros contínuos e sem perdas no InfluxDB.

Visualização fluida e compreensível no Grafana.


O sistema demonstrou excelente desempenho e robustez, indicando forte potencial para uso em protótipos físicos reais.


---

Melhorias Futuras

Construção de protótipo físico para validação em campo

Inclusão de novos sensores (pluviômetro, vazão etc.)

Criação de aplicativo mobile dedicado

Utilização de modelos preditivos de IA para antecipação de enchentes



---

👨‍💻 Autores

Alan Ribeiro do Carmo

Isabella Sofia Martins

Jennifer Aparecida de Sousa Tondade

Ricardo Kiyoshi Kawamuro


Orientado por: Prof. Wallace Rodrigues de Santana
Universidade Presbiteriana Mackenzie — FCI
---
