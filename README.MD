# Projeto de Monitoramento de Temperatura

## Descrição do Funcionamento

Este projeto consiste em um sistema de monitoramento de temperatura para maquinários industriais utilizando um sensor DS18B20 e um microcontrolador ESP32. O sistema mede a temperatura ambiente e, ao detectar uma temperatura que excede um limite pré-definido, ativa um buzzer para emitir um alerta sonoro. Os dados de temperatura são enviados para um servidor MQTT, permitindo monitoramento remoto em tempo real.

### Funcionamento

1. **Sensoriamento**: O sensor DS18B20 mede a temperatura e envia os dados para o ESP32.
2. **Alerta de Superaquecimento**: Se a temperatura exceder um valor limite, o buzzer é acionado.
3. **Comunicação Remota**: As leituras de temperatura são publicadas em um servidor MQTT, permitindo acesso remoto.

## Software Desenvolvido

O software foi desenvolvido em C++ utilizando a plataforma Arduino IDE. O código completo está disponível no repositório.

## Descrição do Hardware Utilizado

- **Microcontrolador**: ESP32
- **Sensor de Temperatura**: DS18B20
- **Atuador**: Buzzer 3V
- **Resistor**: 4.7kΩ (pull-up para o sensor DS18B20)
- **Fonte de Alimentação**: Fonte 3.3V para o ESP32 e sensor
- **Plataforma de Desenvolvimento**: Arduino IDE

### Peças e Dimensões

- **ESP32**: Dimensões padrão de 58mm x 25mm.
- **Sensor DS18B20**: Aproximadamente 15mm de comprimento, 5mm de diâmetro.
- **Buzzer**: Dimensões variáveis, geralmente em torno de 20mm x 20mm.

## Documentação das Interfaces, Protocolos e Módulos de Comunicação

- **Wi-Fi (TCP/IP)**: O ESP32 conecta-se à rede Wi-Fi usando o protocolo TCP/IP.
- **MQTT**: O protocolo MQTT é utilizado para comunicação de dados de temperatura entre o ESP32 e o broker HiveMQ.
  - **Broker**: `broker.hivemq.com`
  - **Tópico**: `seuTopico/temperatura`
  - **Porta**: `1883`

## Considerações Finais

Este projeto oferece uma solução eficaz para o monitoramento de temperatura em ambientes industriais, utilizando sensores de alta precisão e comunicação remota. É ideal para aplicações onde o controle rigoroso da temperatura é crucial para a segurança e desempenho operacional.
