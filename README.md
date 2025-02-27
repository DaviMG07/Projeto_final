# Sistema de Controle para Processo de Plantio, Irrigação e Colheita

## Descrição
Este sistema implementa um controle automatizado para um processo de simulação de plantio, irrigação e colheita utilizando uma máquina de estados. Ele gerencia diversos componentes eletrônicos, como botões com debounce, joystick, LEDs RGB, matriz de LEDs e um display SSD1306 via comunicação I2C.

## Funcionalidades
- Controle de botões com debounce para interação do usuário.
- Leitura e uso de um joystick.
- Controle de LEDs RGB para indicar estados do sistema.
- Gerenciamento de uma matriz de LEDs para visualização do processo.
- Exibição de informações no display OLED SSD1306 via I2C.

## Estados do Sistema
O sistema é baseado em uma máquina de estados finitos, com as seguintes etapas:
1. **POUSIO**: Estado inicial que exibe a grama no display.
2. **PLANTIO**: Simulação do plantio com mudança de cor nos LEDs.
3. **IRRIGAÇÃO**: Exibição do modo de irrigação e atualização do display.
4. **COLHEITA**: Simulação da colheita e retorno ao estado inicial.

## Componentes Utilizados
- **Microcontrolador Raspberry Pi Pico**
- **Botões (Button A, Button B e Joystick)**
- **LEDs RGB**
- **Matriz de LEDs**
- **Display OLED SSD1306**

## Configuração e Pinos
O sistema utiliza os seguintes pinos para comunicação e controle:

| Componente | Porta/Pino |
|------------|------------|
| Display SSD1306 | I2C1 (SDA: 14, SCL: 15) |
| Matriz de LEDs | PIO0, SM0 |
| Botões | GPIO configurados dinamicamente |
| LEDs RGB | GPIO definidos no código |

## Compilação e Execução
1. Certifique-se de ter instalado o SDK do Raspberry Pi Pico.
2. Clone o repositório e navegue até a pasta do projeto.
3. Compile o código com os comandos:
   ```sh
   mkdir build
   cd build
   cmake ..
   make
   ```
4. Envie o binário gerado para o Raspberry Pi Pico.
5. Conecte ao Pico via USB e execute o programa.

## Autores
Davi Macêdo Gomes
Este projeto foi desenvolvido para simular um sistema de plantio automatizado utilizando componentes eletrônicos.

