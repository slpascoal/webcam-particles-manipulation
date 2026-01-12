# 🌌 Cyberpunk Particle Interface

> **Uma experiência interativa de Realidade Aumentada baseada na Web, controlada por gestos manuais e renderizada com 12.000 partículas de alta performance.**

## 📋 Sobre o Projeto

Este projeto é uma aplicação *Single-File* (arquivo único) que combina **Computer Vision** e **WebGL**. Ele utiliza a webcam para rastrear as mãos do usuário em tempo real e permite a manipulação física e visual de um enxame de partículas neon.

O visual é inspirado na estética **Hardcore Cyberpunk**, apresentando scanlines, vinhetas, fontes futuristas e um HUD (Heads-Up Display) funcional.

## ✨ Funcionalidades

* **Rastreamento de Mãos em Tempo Real:** Utiliza MediaPipe Hands para detectar até 2 mãos simultaneamente.
* **Física de Partículas:** 12.000 partículas reagindo a forças de atração, repulsão e turbulência.
* **Reconhecimento de Gestos:** Diferentes contagens de dedos acionam diferentes formas, cores e comportamentos.
* **Modo Espelho:** A imagem da câmera é exibida ao fundo com filtros estilizados, funcionando como um espelho de realidade aumentada.
* **Arquitetura Simples:** Todo o código (HTML, CSS, JS) reside em um único arquivo `index.html`.

## 🚀 Como Executar

### Pré-requisitos

* Um navegador moderno (Chrome, Edge, Firefox) com suporte a WebGL.
* Uma webcam conectada.

### Passo a Passo

1. **Baixe o arquivo:** Salve o código como `index.html`.
2. **Abra no Navegador:**
* **Opção Recomendada (VS Code):** Instale a extensão "Live Server", clique com o botão direito no arquivo e escolha "Open with Live Server".
* **Opção Simples:** Basta arrastar o arquivo `index.html` para dentro de uma aba do Chrome ou clicar duas vezes nele.


3. **Permissões:** Ao abrir, o navegador solicitará permissão para usar a câmera. Clique em **Permitir**.

## 🎮 Guia de Comandos (Gestos)

O sistema diferencia a **Mão Esquerda** (Comandos de Conteúdo) da **Mão Direita** (Interação Física).

### 🖐️ Mão Direita (Controlador de Formas)

A quantidade de dedos levantados altera o texto e a cor das partículas:

| Gesto | Resultado Visual | Cor (Neon) |
| --- | --- | --- |
| **1 Dedo** | Texto: "Hello" | 🔵 Azul (Cyan) |
| **2 Dedos** | Texto: "Gemini3" | 🟡 Amarelo |
| **3 Dedos** | Texto: "非常好用" (Muito Útil) | 🟣 Rosa |
| **4 Dedos** | Texto: "再见" (Tchau) | 🟢 Verde |
| **Palma Aberta** | **Catch Mode:** Prepara atração | --- |

### ✋ Mão Esquerda (Interator Físico)

Controla a física e o comportamento do ambiente:

| Gesto | Efeito |
| --- | --- |
| **Apontar / Punho** | **Repulsão:** As partículas fogem da ponta do seu dedo indicador (apenas no plano 2D). |
| **Palma Aberta (5 Dedos)** | **Modo Nebula:** As partículas se espalham por toda a tela em 3D. Mover a mão cria ondas (efeito de água). |

### 🔥 COMBO ULTIMATE

Quando ambas as mãos estão com a **Palma Aberta (5 dedos)** simultaneamente:

* **Efeito:** As partículas formam uma **Bola de Basquete 3D** giratória sobre a mão esquerda.
* **Comportamento:** As partículas ganham uma trajetória de "quique" energético.

## 🛠️ Tecnologias Utilizadas

* **[Three.js](https://threejs.org/):** Renderização 3D e sistema de partículas.
* **[MediaPipe Hands](https://www.google.com/search?q=https://google.github.io/mediapipe/solutions/hands.html):** Visão computacional e tracking de esqueleto manual.
* **HTML5 / CSS3:** Estrutura e estilização da interface (HUD).

## ⚠️ Solução de Problemas

* **Tela Preta (Sem vídeo):** Verifique se você permitiu o acesso à câmera no topo do navegador. Recarregue a página (F5) se necessário.
* **Lentidão (FPS baixo):** O sistema é pesado graficamente. Feche outras abas ou programas que usem a GPU. Se estiver no notebook, certifique-se de que está conectado à energia.
* **Mãos Trocadas:** O sistema funciona como um espelho. Sua mão esquerda real controla o lado esquerdo da tela (HUD "L.HAND").

---
