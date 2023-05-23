# Sensor Laser Arduino

Este é um projeto de Sensor de Segurança a Laser desenvolvido utilizando Arduino, para a disciplina de Organização e Arquitetura de Computadores.



https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/64d3ac82-7b2d-4261-ac4e-214110074ebb



## Componentes Necessários

- 1 Arduino UNO
- 1 Módulo LDR (Light Dependent Resistor)
- 1 Módulo Laser
- 1 Protoboard
- 1 Buzzer
- 5 Jumpers

## Montagem do Circuito

1. Conecte o Arduino UNO à protoboard.
2. Conecte o módulo LDR ao Arduino utilizando 3 jumpers:
   - Conecte o pino GND do módulo LDR ao pino GND do Arduino.
   - Conecte o pino VCC do módulo LDR ao pino 5V do Arduino.
   - Conecte o pino de saída (S) do módulo LDR ao pino A0 (entrada analógica) do Arduino.
3. Conecte o módulo Laser ao Arduino utilizando 2 jumpers:
   - Conecte o pino positivo do módulo Laser ao pino 13 (saída digital) do Arduino.
   - Conecte o pino negativo do módulo Laser ao pino GND do Arduino.
4. Conecte o buzzer ao Arduino utilizando 2 jumpers:
   - Conecte o pino positivo do buzzer ao pino 12 (saída digital) do Arduino.
   - Conecte o pino negativo do buzzer ao pino GND do Arduino.

Certifique-se de seguir corretamente as conexões descritas acima para evitar danos aos componentes.

## Funcionamento

O Sensor de Segurança a Laser utiliza o módulo LDR para detectar se o feixe de luz do laser está sendo interrompido. Quando o feixe de luz é bloqueado, o módulo LDR registra a mudança na intensidade da luz e envia um sinal analógico para o Arduino.

O Arduino, então, verifica o valor lido pelo módulo LDR. Se o valor estiver abaixo de um determinado limite pré-estabelecido, indica que o feixe de luz está bloqueado e aciona o módulo buzzer para emitir um alerta sonoro.

## Alimentação

O Arduino UNO pode ser alimentado através de uma fonte de energia externa (por exemplo, um adaptador de 9V) ou via USB, conectando-o a um computador. O módulo LDR pode ser alimentado pelo próprio Arduino ou por uma fonte de energia separada, desde que a polaridade esteja cor
