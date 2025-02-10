# embarcatech_2025_u4c6_Interfaces_serial
#Relatório do Projeto: Comunicação Serial e Controle de LEDs no RP2040
1. Introdução
Este projeto tem como objetivo consolidar os conhecimentos sobre comunicação serial em microcontroladores, utilizando a placa de desenvolvimento BitDogLab baseada no RP2040. Durante a implementação, foram explorados os protocolos UART e I2C, a manipulação de LEDs comuns e LEDs endereçáveis WS2812, e a integração de botões com interrupções e debounce via software.

2. Objetivos
Compreender e aplicar comunicação serial (UART e I2C) no RP2040.
Implementar o controle de LEDs comuns e LEDs endereçáveis WS2812.
Utilizar interrupções (IRQ) para a interação com botões.
Aplicar técnicas de debounce via software para evitar leituras incorretas dos botões.
Exibir informações no display SSD1306 (I2C) e registrar eventos via Serial Monitor (UART).
Desenvolver um código bem estruturado e comentado.
3. Materiais Utilizados
Placa de desenvolvimento BitDogLab (RP2040)
Matriz de LEDs 5x5 WS2812 (conectada ao GPIO 7)
LED RGB (GPIOs 11, 12 e 13)
Botão A (GPIO 5)
Botão B (GPIO 6)
Display SSD1306 (I2C – GPIOs 14 e 15)
4. Implementação
4.1. Modificação da Biblioteca font.h
Para exibição de caracteres no display SSD1306, foram adicionados caracteres minúsculos à biblioteca font.h, permitindo uma melhor exibição de informações no display.

4.2. Comunicação Serial via UART
O Serial Monitor do VS Code foi utilizado para permitir a entrada de caracteres, os quais eram exibidos no display SSD1306.

Quando um número entre 0 e 9 era digitado, um símbolo correspondente era exibido na matriz de LEDs WS2812.
4.3. Interação com os Botões
Botão A: Alternava o estado do LED Verde, registrando a mudança no display SSD1306 e no Serial Monitor.
Botão B: Alternava o estado do LED Azul, seguindo a mesma lógica de exibição de mensagens.
Ambas as interações foram implementadas utilizando interrupções (IRQ) para evitar polling contínuo e melhorar a eficiência do sistema.
4.4. Implementação do Debounce via Software
O efeito bouncing dos botões foi tratado por meio de debounce via software, garantindo leituras estáveis e evitando múltiplos acionamentos indesejados.

5. Resultados Obtidos
A comunicação serial via UART funcionou corretamente, permitindo a entrada de caracteres e exibição no display SSD1306.
Os LEDs foram controlados com sucesso, incluindo a matriz WS2812 e o LED RGB.
O uso de interrupções possibilitou um controle eficiente dos botões sem consumir processamento desnecessário.
O debounce via software eliminou leituras incorretas dos botões, garantindo respostas confiáveis.
O código foi bem estruturado e comentado, seguindo boas práticas de programação para sistemas embarcados.

6. Conclusão
O projeto foi concluído com sucesso, integrando comunicação serial, controle de LEDs e botões, utilizando as funcionalidades da placa BitDogLab (RP2040). O uso de interrupções e debounce garantiu um sistema eficiente e responsivo. A simulação e testes em hardware confirmaram o funcionamento esperado, consolidando o aprendizado sobre interfaces de comunicação serial e manipulação de periféricos no RP2040.
7. LINK DO VÍDEO:
   
8. Referências
Documentação do Pico SDK
Datasheets do RP2040 e do Display SSD1306
Materiais didáticos da disciplina
