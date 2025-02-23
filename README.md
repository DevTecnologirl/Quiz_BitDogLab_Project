# 💡 Controle de LEDs WS2812, Display SSD1306 e Comunicação Serial com RP2040

## 📝 Sobre o Projeto
Este projeto explora o uso da comunicação serial (UART e I2C) e o controle de LEDs na placa BitDogLab (RP2040). Ele permite operar uma matriz 5x5 de LEDs WS2812, exibir informações em um display OLED SSD1306 e interagir com botões físicos utilizando interrupções.

### 🎯 Principais Objetivos:
- Implementar comunicação serial (UART e I2C) com microcontroladores.
- Controlar LEDs endereçáveis WS2812 e LEDs RGB comuns.
- Aplicar técnicas de debouncing para botões.
- Utilizar interrupções (IRQ) para capturar eventos.
- Permitir entrada de caracteres pelo Serial Monitor e exibição no display SSD1306.

## 📌 Requisitos Necessários
- Placa BitDogLab
- VS Code
- Extensão Raspberry Pi Pico
- SDK do Raspberry Pi Pico
- CMake para compilação
- MinGW (Windows) ou GCC (Linux/macOS) para compilar

## 🔧 Componentes do Projeto
- **BitDogLab (RP2040)**
- **Matriz de LEDs WS2812 (5x5)** → GPIO 7
- **LED RGB** → GPIOs 11, 12 e 13
- **Botão A** → GPIO 5
- **Botão B** → GPIO 6
- **Display SSD1306 (I2C)** → GPIOs 14 e 15

## 🚀 Funcionalidades Implementadas
Foi modificado a cor do LED para RED e mantendo o GREEN para o projeto quiz (True/False)
A ideia é aproveitar a escolha no serial do número de sua pergunta e ao responder quem controla a BitDogLab emite TRUE com o Button A e FALSE com o Button B. No intervalo emite "Próxima pergunta".

### 🖋️ Modificação da Biblioteca `font.h`
✅ Adicionada compatibilidade com caracteres minúsculos.

### ⌨️ Entrada de Caracteres via UART
✅ O que for digitado no Serial Monitor aparece no display SSD1306.
✅ Números (0-9) ativam símbolos específicos na matriz WS2812.

### 🔘 Interação com Botões
- **Botão A**:
  - ✅ Alterna o LED Verde (ligado/desligado).
  - ✅ Atualiza o estado no display SSD1306 e no Serial Monitor.
- **Botão B**:
  - ✅ Alterna o LED Vermelho (ligado/desligado).
  - ✅ Exibe o estado no display SSD1306 e no Serial Monitor.

## 📂 Organização do Projeto
O código foi escrito em C, a estrutura de diretórios facilita o desenvolvimento e a compilação no VS Code com a extensão Raspberry Pi Pico.

### 🔍 Estrutura dos Diretórios:
- ```src/``` → Código-fonte principal (`main.c`).
- ```src/lib/``` → Bibliotecas (`.h`) e suas implementações.

## 🛠️ Como Configurar e Executar

1. Clone este repositório:
   ```bash
   git clone (https://github.com/DevTecnologirl/Quiz_BitDogLab_Project)
   ```
2. Abra o projeto no **VS Code**.
3. Certifique-se de que a extensão **Raspberry Pi Pico** está instalada e configurada.
4. Importe o projeto para gerar a pasta `build` automaticamente.
5. Compile o código através da opção **Compilar Projeto**.
6. Coloque a **BitDogLab** no modo **BOOTSEL** e carregue o software.
7. Acesse o **Monitor Serial** no VS Code e habilite a opção `Toggle Terminal Mode`.
8. Selecione `Start Monitoring` e pressione `ENTER` para abrir o menu principal.

2. Use o site para clonar do git para o explorer: 
    https://download-directory.github.io/

## 🎥 Vídeo Demonstrativo
🔗 [Veja o projeto rodando na BitDogLab]

Este vídeo demonstra:
- O funcionamento do código na placa BitDogLab.
- A interação com LEDs e botões.
- A exibição de caracteres no display SSD1306.

---

📌 **Projeto EmbarcaTech 2025 - Camilly Duarte**
📌 **Código adaptado - Credits: Davimmo**
