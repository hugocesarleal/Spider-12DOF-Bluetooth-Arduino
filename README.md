# Robô Aranha Quadrúpede 12 DOF - Controle Bluetooth

Este repositório contém o código-fonte para um robô quadrúpede articulado com **12 Graus de Liberdade (DOF)**, desenvolvido como parte das atividades do **Laboratório Maker - Canastra Hub** no **IFMG Campus Bambuí**. O projeto visa construir uma plataforma robótica para estudos de cinemática e estabilidade dinâmica, utilizando fabricação digital e controle via Bluetooth através de um aplicativo móvel.

## 🕷️ Sobre o Projeto

O robô baseia-se no design de código aberto de *RegisHsu* e utiliza uma configuração de **3 servomotores por perna**, permitindo movimentos sofisticados como caminhada omnidirecional, rotação e rotinas de dança.

### Funcionalidades Principais
* **Locomoção**: Caminhada para a frente, para trás e rotação (esquerda/direita).
* **Interação**: Acenar, apertar a mão e realizar rotinas de dança.
* **Interface Visual**: Suporte para tela OLED para exibição de status.
* **Controle Sem Fio**: Comandos recebidos via Bluetooth através do módulo HC-05.

## 🛠️ Hardware Necessário

* **Microcontrolador**: Arduino Nano.
* **Atuadores**: 12 Servomotores (SG90 ou MG90).
* **Expansão**: Shield de expansão para Arduino Nano.
* **Comunicação**: Módulo Bluetooth HC-05.
* **Tela**: OLED SSD1306 via I2C.
* **Estrutura**: Peças impressas em 3D utilizando aproximadamente 100g de filamento PLA.

## 💻 Bibliotecas Requeridas

Para compilar o código, é necessário instalar as seguintes bibliotecas na Arduino IDE:
* `Servo.h`
* `FlexiTimer2.h`
* `Wire.h`
* `Adafruit_SSD1306.h`
* `Adafruit_GFX.h`

## 📱 Comandos de Controle (Bluetooth)

O robô processa os seguintes caracteres recebidos via Serial para a execução de ações:

| Caractere | Ação |
| :--- | :--- |
| **F** | Passo para a frente |
| **B** | Passo para trás |
| **L** | Virar para a esquerda |
| **R** | Virar para a direita |
| **N** | Ficar em pé (Stand) |
| **n** | Sentar (Sit) |
| **M** / **m** | Apertar a mão (Hand Shake) |
| **X** | Executar rotina de dança (Body Dance) |
| **Y** | Acenar (Hand Wave) |

## 🚀 Como Usar

1.  **Montagem**: Ligue os servos seguindo as definições de pinos no código: `{3, 4, 2}, {6, 7, 5}, {9, 8, 10}, {12, 11, 13}`.
2.  **Upload**: Carregue o arquivo `.ino` para o seu Arduino Nano.
3.  **Conexão**: Pareie o dispositivo móvel com o módulo HC-05.
4.  **Controle**: Utilize o aplicativo customizado desenvolvido pela **FAST (Fábrica de Soluções Tecnológicas)** para enviar os comandos.

## 🤝 Créditos e Referências

* **Design Original**: [RegisHsu no Thingiverse](https://www.thingiverse.com/thing:1009659).
* **Base do Código**: Robot Lk.
* **Desenvolvimento e Adaptação**: Hugo Cesar Leal.
* **Instituição**: IFMG Campus Bambuí - Laboratório Maker.

---
### Referências Institucionais
* Projeto: DESENVOLVIMENTO DE ROBÔ QUADRÚPEDE 12 DOF COM CONTROLE MOBILE VIA BLUETOOTH (IFMG Campus Bambuí).
* Código-fonte Arduino: Robo_aranha_bluetooth.ino.
