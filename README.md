# 🕵️ Chatbot Interrogatório Noir (Rasa)

## 📌 Descrição do Projeto

Este projeto consiste no desenvolvimento de um chatbot utilizando o framework **Rasa**, com uma interface web personalizada em HTML, CSS e JavaScript.

O chatbot simula um **interrogatório policial em estilo noir**, onde o usuário assume o papel de um **suspeito** e interage com um detetive que conduz uma investigação sobre o desaparecimento de um relógio de ouro.

O sistema foi projetado como um **mini jogo investigativo**, permitindo diferentes tipos de interação como:

* Apresentar álibis
* Negar envolvimento
* Pedir pistas
* Acusar outros personagens
* Confessar o crime

---

## 🎯 Objetivo

O objetivo do projeto é aplicar conceitos de:

* Processamento de Linguagem Natural (NLP)
* Criação de intents e fluxos conversacionais
* Integração entre frontend e backend
* Experiência do usuário em interfaces conversacionais

---

## 🎨 Interface do Chatbot

A interface foi desenvolvida com foco em imersão, utilizando um tema visual inspirado em filmes noir:

* 🌑 Tema escuro com iluminação suave
* ⌨️ Efeito de digitação nas respostas
* 🔊 Som de máquina de escrever
* ⏳ Delay nas respostas (simula raciocínio do detetive)
* 🧑 Usuário identificado como **"Suspeito"**

---

## 🧠 Tecnologias Utilizadas

* **Rasa** (NLP e backend conversacional)
* **Python 3.10**
* **HTML, CSS e JavaScript** (interface)
* **Fetch API** (comunicação com o Rasa)

---

## 📁 Estrutura do Projeto

```
chatbot-noir/
│
├── index.html
│
└── rasa/
    ├── config.yml
    ├── domain.yml
    └── data/
        ├── nlu.yml
        ├── stories.yml
        └── rules.yml
```

---

## ⚙️ Como Executar o Projeto

### 1. Pré-requisitos

* Python **3.10**
* pip instalado
* Git (opcional)

---

### 2. Criar ambiente virtual

```bash
py -3.10 -m venv rasa_env
```

Ativar:

```bash
rasa_env\Scripts\activate
```

---

### 3. Instalar o Rasa

```bash
pip install rasa
```

---

### 4. Treinar o modelo

Acesse a pasta do Rasa:

```bash
cd rasa
```

Execute:

```bash
rasa train
```

---

### 5. Iniciar o servidor

```bash
rasa run --enable-api --cors "*"
```

O servidor será iniciado em:

```
http://localhost:5005
```

---

### 6. Executar a interface

Abra o arquivo:

```
index.html
```

no navegador.

---

## 💬 Exemplos de Interação

```
Usuário: oi
Bot: Finalmente apareceu. Sente-se, Suspeito...

Usuário: qual é o caso?
Bot: O relógio de ouro do prefeito desapareceu...

Usuário: eu estava no bar
Bot: Um álibi conveniente...

Usuário: você tem alguma pista?
Bot: Encontramos uma luva preta perto da janela...

Usuário: eu confesso
Bot: Então temos uma confissão...
```

---

## 🎮 Exemplos de Jogabilidade (Roteiros)

### 🟢 Roteiro 1 — Suspeito Inocente

```
Usuário: oi
Bot: inicia o interrogatório.

Usuário: qual é o caso?
Bot: explica o sumiço do relógio.

Usuário: onde aconteceu o crime?
Bot: explica que foi no Hotel Neblina.

Usuário: eu estava no bar
Bot: comenta que o álibi é conveniente.

Usuário: quais evidências existem?
Bot: fala da luva preta, lama e testemunha.

Usuário: essa luva não é minha
Bot: questiona a negação da pista.

Usuário: quem são os suspeitos?
Bot: cita outros suspeitos.

Usuário: eu quero cooperar
Bot: aceita a cooperação.

Usuário: eu provei minha inocência
Bot: encerra dizendo que, por enquanto, a história se sustenta.
```

---

### 🔴 Roteiro 2 — Suspeito Culpado

```
Usuário: boa noite
Bot: inicia o interrogatório.

Usuário: do que eu sou acusado?
Bot: explica o caso do relógio sumido.

Usuário: eu não fiz nada
Bot: desconfia da negação.

Usuário: eu estava no corredor
Bot: registra o álibi.

Usuário: você tem alguma pista?
Bot: apresenta a luva preta e marcas de lama.

Usuário: foi o mordomo
Bot: reage à acusação contra outra pessoa.

Usuário: na verdade eu estava em outro lugar
Bot: aponta contradição na história.

Usuário: estou nervoso
Bot: comenta o nervosismo.

Usuário: tudo bem, eu confesso
Bot: encerra com a confissão.
```

---

## 🔄 Fluxo Conversacional

O chatbot foi estruturado utilizando:

* **Intents** → reconhecimento das intenções do usuário
* **Stories** → fluxo principal da conversa
* **Rules** → respostas fixas para determinados cenários

O fluxo simula um interrogatório dinâmico com múltiplas possibilidades.

---

## 🚀 Melhorias Implementadas

* Interface personalizada e temática
* Delay nas respostas para maior realismo
* Efeito de digitação com áudio
* Estrutura de mini jogo investigativo
* Integração completa frontend + backend

---

## 📌 Considerações Finais

Este projeto demonstra como é possível criar experiências interativas e imersivas utilizando chatbots, combinando técnicas de NLP com design de interface.

Além disso, o uso do Rasa permite a construção de fluxos conversacionais mais sofisticados e controlados, sendo uma excelente ferramenta para aplicações reais.

---
