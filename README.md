# [cite_start]Robô Aranha Quadrúpede 12 DOF - Controlo Bluetooth [cite: 1]

[cite_start]Este repositório contém o código-fonte para um robô quadrúpede articulado com **12 Graus de Liberdade (DOF)** [cite: 39][cite_start], desenvolvido como parte das atividades do **Laboratório Maker - Canastra Hub** no **IFMG Campus Bambuí**[cite: 1]. [cite_start]O projeto visa construir uma plataforma robótica para estudos de cinemática e estabilidade dinâmica [cite: 2][cite_start], utilizando fabricação digital e controlo via Bluetooth através de uma aplicação móvel[cite: 1].

## 🕷️ Sobre o Projeto

[cite_start]O robô baseia-se no design de código aberto de *RegisHsu* [cite: 17, 36] [cite_start]e utiliza uma configuração de **3 servomotores por perna** [cite: 39][cite_start], permitindo movimentos sofisticados como caminhada omnidirecional, rotação e rotinas de dança[cite: 7, 9, 34].

### Funcionalidades Principais
* [cite_start]**Locomoção**: Caminhada para a frente, para trás e rotação (esquerda/direita)[cite: 60, 61, 62, 63].
* [cite_start]**Interação**: Acenar, apertar a mão e realizar rotinas de dança[cite: 65, 67, 71].
* [cite_start]**Interface Visual**: Suporte para ecrã OLED para exibição de status[cite: 38].
* [cite_start]**Controlo Sem Fios**: Comandos recebidos via Bluetooth através do módulo HC-05[cite: 30, 60].

## 🛠️ Hardware Necessário

* [cite_start]**Microcontrolador**: Arduino Nano[cite: 27].
* [cite_start]**Atuadores**: 12 Servomotores (SG90 ou MG90)[cite: 28, 39].
* [cite_start]**Expansão**: Shield de expansão para Arduino Nano[cite: 29].
* [cite_start]**Comunicação**: Módulo Bluetooth HC-05[cite: 30].
* [cite_start]**Ecrã**: OLED SSD1306 via I2C[cite: 38].
* [cite_start]**Estrutura**: Peças impressas em 3D utilizando aproximadamente 100g de filamento PLA[cite: 23].

## 💻 Bibliotecas Requeridas

[cite_start]Para compilar o código, é necessário instalar as seguintes bibliotecas na Arduino IDE[cite: 38]:
* `Servo.h`
* `FlexiTimer2.h`
* `Wire.h`
* `Adafruit_SSD1306.h`
* `Adafruit_GFX.h`

## 📱 Comandos de Controlo (Bluetooth)

[cite_start]O robô processa os seguintes caracteres recebidos via Serial para a execução de ações [cite: 60-75]:

| Caractere | Ação |
| :--- | :--- |
| **F** | [cite_start]Passo para a frente [cite: 60] |
| **B** | [cite_start]Passo para trás [cite: 61] |
| **L** | [cite_start]Virar para a esquerda [cite: 62] |
| **R** | [cite_start]Virar para a direita [cite: 63] |
| **N** | [cite_start]Ficar em pé (Stand) [cite: 64] |
| **n** | [cite_start]Sentar (Sit) [cite: 65] |
| **M** / **m** | [cite_start]Apertar a mão (Hand Shake) [cite: 66, 67] |
| **X** | [cite_start]Executar rotina de dança (Body Dance) [cite: 68] |
| **Y** | [cite_start]Acenar (Hand Wave) [cite: 72] |

## 🚀 Como Usar

1.  [cite_start]**Montagem**: Ligue os servos seguindo as definições de pinos no código: `{3, 4, 2}, {6, 7, 5}, {9, 8, 10}, {12, 11, 13}`[cite: 39].
2.  [cite_start]**Upload**: Carregue o ficheiro `.ino` para o seu Arduino Nano[cite: 58].
3.  [cite_start]**Ligação**: Emparelhe o dispositivo móvel com o módulo HC-05[cite: 30].
4.  [cite_start]**Controlo**: Utilize a aplicação customizada desenvolvida pela **FAST (Fábrica de Soluções Tecnológicas)** para enviar os comandos[cite: 9, 13, 26].

## 🤝 Créditos e Referências

* [cite_start]**Design Original**: [RegisHsu no Thingiverse](https://www.thingiverse.com/thing:1009659)[cite: 36].
* [cite_start]**Base do Código**: Robot Lk[cite: 38].
* [cite_start]**Desenvolvimento e Adaptação**: Hugo Cesar Leal[cite: 1].
* [cite_start]**Instituição**: IFMG Campus Bambuí - Laboratório Maker[cite: 1].

---
### Referências
* [1] Projeto: DESENVOLVIMENTO DE ROBÔ QUADRÚPEDE 12 DOF COM CONTROLE MOBILE VIA BLUETOOTH (IFMG Campus Bambuí).
* [2] Código-fonte Arduino: Robo_aranha_bluetooth.ino.
