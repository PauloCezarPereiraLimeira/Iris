<h1 align="center">
🤖 IRIS – Plataforma de Robótica Social com Inteligência Emocional Artificial
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/IA%20Humanizada-%2300ffff?style=for-the-badge&logo=openai&logoColor=white" alt="IA Humanizada" />
  <img src="https://img.shields.io/badge/Pesquisa%20Científica-%230099ff?style=for-the-badge&logo=academia&logoColor=white" alt="Pesquisa Científica" />
  <img src="https://img.shields.io/badge/Rob%C3%B3tica%20Social-%23ff00ff?style=for-the-badge&logo=raspberrypi&logoColor=white" alt="Robótica Social" />
</p>

---

## 🌐 Visão Geral

**IRIS** é uma robô social modular, impulsionada por inteligência emocional artificial, que integra tecnologias de aprendizado de máquina e robótica acessível para proporcionar interações humano-máquina altamente significativas e inclusivas.

> *Missão:* Democratizar a robótica social com um sistema empático e adaptativo, aplicável em educação, saúde mental e inclusão social.

---

## 🎯 Objetivos Estratégicos

- **🛠️ Desenvolvimento de um robô social acessível, escalável e de fácil replicação.**  
- **🧠 Integração entre IA generativa e sensores físicos para simular empatia e cognição autêntica.**  
- **🔬 Viabilização de pesquisas acadêmicas e aplicações clínicas em contextos de saúde e educação.**  
- **🚀 Estímulo à colaboração entre academia, indústria e aceleradoras para ampliação de ecossistema.**

---

## 🧱 Arquitetura Modular & Responsabilidades

### 👤 Pessoa 1 – Backend Embarcado e Controle Físico  
**Missão:** Orquestrar a comunicação e controle do hardware, garantindo robustez e confiabilidade no corpo físico.

- Implementar comunicação serial e protocolos (I2C, PWM, GPIO).  
- Desenvolver drivers para sensores e atuadores.  
- Criar Máquina de Estados Finitos para gerenciar comportamentos.  
- Expor APIs REST/WebSocket para integração com IA.  
- Automatizar inicialização e monitoramento via SystemD/supervisord.

**Stack:** Python 3.10+, C++, FastAPI, RPi.GPIO, pyserial.

---

### 👤 Pessoa 2 – Núcleo de Inteligência Artificial (IA e Percepção)  
**Missão:** Desenvolver o cérebro da IRIS para percepção, cognição e comunicação natural.

- Pipeline completo de áudio: captura, detecção de voz e transcrição offline (Whisper.cpp, Vosk).  
- Implementação de modelo de linguagem local (Mistral 7B via Ollama).  
- Geração de respostas com personalidade e contexto emocional.  
- Percepção visual para reconhecimento facial e emoções (OpenCV).  
- Memória episódica para aprendizagem contínua (SQLite/TinyDB).

**Stack:** Python, OpenCV, dlib, whisper.cpp, Vosk, Ollama.

---

### 👤 Pessoa 3 – Interface Visual (HUD e Expressividade Facial)  
**Missão:** Criar uma interface visual expressiva e interativa para o "rosto" da IRIS.

- Desenvolvimento UI com Pygame/Kivy para hardware embarcado.  
- Animações dinâmicas: olhos, emoções, reatividade ao ambiente.  
- HUD para status da IA e diagnósticos em tempo real.  
- Sincronização visual via WebSocket/REST.

**Stack:** Python, Kivy, Pygame, WebSocket, MQTT.

---

### 👤 Pessoa 4 – Arquiteto de Integração e Orquestração  
**Missão:** Integrar todos os módulos em um sistema coeso, resiliente e escalável.

- FSM mestre para orquestração dos estados globais da IRIS.  
- Implementação de broker MQTT/Redis para comunicação desacoplada.  
- Desenvolvimento de painel de monitoramento e logs automáticos.  
- Automação de reinício e watchdog via SystemD.

**Stack:** Python, MQTT (Mosquitto), Redis, SystemD, logrotate.

---

---

## 🎯 Casos de Uso Estratégicos

    👨‍🏫 Educação: Interação em escolas, museus e centros de aprendizagem.

    👵 Saúde e Bem-estar: Companheirismo para idosos e apoio a pessoas com necessidades especiais.

    🎤 Eventos: Apresentação digital e interação em feiras e conferências.

    🧪 Pesquisa: Plataforma para experimentos em IHC e robótica social.

📸 Protótipo IRIS
<p align="center">
<img src="https://raw.githubusercontent.com/PauloCezarPereiraLimeira/IRIS/main/images/iris-prototype.png" width="600" alt="Protótipo IRIS" />
</p>
<p align="center">
<img src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif" width="200" alt="Animação IRIS" />
</p>

## 🧠 Diagrama Funcional

```mermaid
graph TD
  A[Usuário] -->|Fala| B[🎤 Reconhecimento de Voz]
  B --> C[🧠 NLP + LLM]
  C --> D[💬 Respostas Inteligentes]
  C --> E[🎭 Comandos de Expressão]
  D -->|Texto| F[🔊 Síntese de Voz]
  E --> G[🦾 Atuadores e Animações]
  F --> H[🔊 Fala da IRIS]


