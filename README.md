# Sensor Laser Arduino

Este é um projeto de Sensor de Segurança a Laser desenvolvido utilizando Arduino, para a disciplina de Organização e Arquitetura de Computadores.



https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/64d3ac82-7b2d-4261-ac4e-214110074ebb



## Componentes Necessários

- 1 Arduino UNO
- 1 Módulo LDR (Light Dependent Resistor)
- 1 Módulo Laser
- 1 Protoboard
- 1 Buzzer
- 6 Jumpers

- Uma fonte de alimentação para o Laser (No projeto foi utilizado outro Arduino, porém não é necessário, apenas para alimentar o laser)

## Montagem do Circuito

### No primeiro Arduino:

1. Conecte o módulo LDR à protoboard.
2. Conecte o módulo LDR ao Arduino utilizando 3 jumpers:
   - Conecte o pino GND do módulo LDR ao pino GND do Arduino.
   - Conecte o pino VCC do módulo LDR ao pino 5V do Arduino.
   - Conecte o pino de saída (S) do módulo LDR ao pino 2 (entrada digital) do Arduino.
3. Conecte o buzzer ao Arduino utilizando 2 jumpers:
   - Conecte o pino positivo do buzzer ao pino 8 (saída digital) do Arduino.
   - Conecte o pino negativo do buzzer ao pino segundo GND do Arduino.
  
### No Segundo Arduino:

  1. Conecte o módulo Laser ao Arduino utilizando 2 jumpers:
   - Conecte o pino positivo do módulo Laser (Representado como S) ao pino 5V do Arduino.
   - Conecte o pino negativo do módulo Laser ao pino GND do Arduino.
   
## Funcionamento

O Sensor de Segurança a Laser utiliza o módulo LDR para detectar se o feixe de luz do laser está sendo interrompido. Quando o feixe de luz é bloqueado, o módulo LDR registra a mudança na intensidade da luz e envia um sinal analógico para o Arduino.

O Arduino, então, verifica o valor lido pelo módulo LDR. Se o valor estiver abaixo de um determinado limite pré-estabelecido, indica que o feixe de luz está bloqueado e aciona o módulo buzzer para emitir um alerta sonoro.

## Alimentação

O Arduino UNO pode ser alimentado através de uma fonte de energia externa (por exemplo, um adaptador de 9V) ou via USB, conectando-o a um computador. O módulo LDR pode ser alimentado pelo próprio Arduino ou por uma fonte de energia separada, desde que a polaridade esteja cor

## Explicação do Código

### Código no Arquivo ".txt"

Este código implementa o funcionamento do sensor de laser no Arduino. Ele utiliza dois pinos digitais: um para o sensor (DETECT, pino 2) e outro para realizar uma ação quando o laser é detectado (ACTION, pino 8).

No setup(), o código configura a comunicação serial para imprimir mensagens de teste. Além disso, define os pinos DETECT e ACTION como entrada e saída, respectivamente.

No loop(), o código lê o estado do sensor de laser utilizando a função digitalRead(DETECT) e armazena o valor na variável detected. Se o valor lido for HIGH, indica que o laser foi detectado e, portanto, o pino ACTION é definido como baixo (LOW). É impressa a mensagem "Detected!" no monitor serial.

Caso contrário, se o valor lido for LOW, indica que o laser não está sendo detectado e o pino ACTION é definido como alto (HIGH). É impressa a mensagem "No laser" no monitor serial.

Após isso, há um atraso de 200 milissegundos antes de repetir o loop novamente.

Certifique-se de ter definido corretamente os pinos DETECT e ACTION de acordo com a sua montagem física do circuito.

## Colaboradores

### Aldo Souza: [https://github.com/aldocsouza](https://github.com/aldocsouza)
### Marcos Paulo: https://github.com/Mp455

## Fotos do Projeto


![WhatsApp Image 2023-04-01 at 20 15 52](https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/7bd13bb3-6429-4a5d-8503-dc1519dc0509)

![WhatsApp Image 2023-04-01 at 20 17 51](https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/324cd198-55a0-40bb-9bfa-ecdad880eb8c)

![WhatsApp Image 2023-04-01 at 20 02 15](https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/955339c3-9396-4456-a2e0-d76afdf38e88)

![image](https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/0b4bac15-a3f6-4f49-bcfa-e581166f75ad)

![image](https://github.com/LuiVLoureiro/Sensor-Laser-Arduino/assets/103609685/d6641e8d-9b9e-4bd2-95fc-5f468d68b62f)

