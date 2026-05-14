                                                                                                                                                                        # 📊 Sistema de Monitoramento de Vinheria com Arduino

## 📝 Descrição do Projeto

Este projeto foi desenvolvido para a **Vinheria Agnello** com o objetivo de monitorar as condições ideais de armazenamento dos vinhos utilizando a plataforma Arduino.

O sistema realiza o monitoramento de:

- 🌡️ Temperatura  
- 💧 Umidade  
- 💡 Luminosidade  

As informações são exibidas em tempo real em um display LCD e o sistema utiliza LEDs e buzzer para alertar quando alguma condição está fora do padrão ideal para conservação dos vinhos.

---

## ⚙️ Funcionamento

O sistema faz leituras periódicas dos sensores conectados ao Arduino e classifica o ambiente de acordo com os limites definidos no código.

### 🌡️ Temperatura
- Entre **10°C e 15°C** → condição ideal  
- Abaixo de 10°C → temperatura baixa  
- Acima de 15°C → temperatura alta  

### 💧 Umidade
- Entre **50% e 70%** → condição ideal  
- Abaixo de 50% → umidade baixa  
- Acima de 70% → umidade alta  

### 💡 Luminosidade
- Ambiente escuro → condição ideal  
- Alta luminosidade → condição inadequada para conservação dos vinhos  

---

## 🚦 Sinalização do Sistema

### 🟢 LED Verde
Indica que:
- Temperatura está ideal  
- Umidade está ideal  
- Luminosidade está adequada  

Buzzer desligado.

---

### 🟡 LED Amarelo
Indica problema relacionado à:
- Temperatura fora da faixa ideal  

Buzzer acionado.

---

### 🔴 LED Vermelho
Indica problema relacionado à:
- Umidade fora da faixa ideal  
ou
- Luminosidade excessiva  

Buzzer acionado.

---

## 🧠 Funcionamento do Código

O código foi desenvolvido utilizando o Arduino IDE e as bibliotecas `LiquidCrystal_I2C` e `Wire` para controle do display LCD. (no Tinkercad)

### Principais funcionalidades:
- Leitura dos sensores analógicos
- Média de leituras para reduzir ruídos
- Atualização automática a cada 5 segundos
- Exibição das informações no display LCD
- Acionamento automático dos LEDs e buzzer conforme o estado do ambiente
- Exibição de dados no Monitor Serial

### Sensores utilizados:
- LDR → luminosidade
- Sensor analógico → temperatura
- Sensor analógico → umidade

---

## 🔩 Componentes Utilizados

- 1x Arduino Uno  
- 1x Sensor LDR  
- 1x Sensor de temperatura analógico  
- 1x Sensor de umidade analógico  
- 1x Display LCD I2C 16x2  
- 3x LEDs (verde, amarelo e vermelho)  
- 3x Resistores 220Ω  
- 1x Resistor 10kΩ  
- 1x Buzzer  
- 1x Protoboard  
- Jumpers  

---

## 🔌 Montagem do Circuito

### Sensores
- LDR → A0  
- Temperatura → A1  
- Umidade → A2  

### LEDs
- LED Verde → Pino 10  
- LED Amarelo → Pino 11  
- LED Vermelho → Pino 12  

### Buzzer
- Pino 8  

### Display LCD I2C
- SDA → A4  
- SCL → A5  
- VCC → 5V  
- GND → GND  

---

## 💻 Dependências

- Arduino IDE  
- Bibliotecas:
  - `LiquidCrystal_I2C`
  - `Wire`

---

## ▶️ Como Executar o Projeto

1. Instale a Arduino IDE  
2. Monte o circuito na protoboard ou no simulador  
3. Conecte o Arduino via USB  
4. Abra o código do projeto  
5. Selecione:
   - Placa: Arduino Uno
   - Porta correta
6. Faça o upload do código  
7. Observe o funcionamento no LCD, LEDs e buzzer  

---

## 🧪 Monitor Serial

O sistema também envia informações para o Monitor Serial, exibindo:
- Luminosidade
- Temperatura
- Umidade

Atualização realizada a cada 5 segundos.

---

## 🔗 Simulação no Tinkercad

https://www.tinkercad.com/things/3UBnYi2Emj0-monitoramento-vinheira-cp-2/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fall&sharecode=8a5WZ7S5V4yVZX3xBJOEnjDlYGXDH7Ea2hV6H2wOJVc

---

## 👥 Integrantes

- Gabriel Freitas da Silva Carvalho — RM 570881  
- Erick Martins Picolo — RM 572892  
- Guilherme Marcon Dantas — RM 572171  
- Luiz Felipe Cardoso de Oliveira — RM 569782
