```
# FeiraLocal 🌱 — Marketplace Agrícola Acessível (Front-End Web)

&gt; **Trabalho Prático: Projeto de Design UX/UI e Arquitetura de Interface (Atividade II)**  
&gt; **Disciplina:** Interfaces Digitais UX/UI  
&gt; **Docente:** Prof. Me. Edgar Natanael de Vasconcelos Gregório  
&gt; **Instituição:** Faculdade ESUDA (2026)  
&gt; **Link da Aplicação ao Vivo:** [Acessar FeiraLocal Web no GitHub Pages]([suspicious link removed])

---

## 👥 Integrantes da Equipe
* **Luiz Claudio Martins**
* **Gabriel Normandio**
* **Pethrus Souza**

---

## 📌 Contexto e Origem do Projeto

O **FeiraLocal** é um produto digital concebido para solucionar o abismo tecnológico e operacional que separa pequenos produtores rurais da agricultura familiar dos consumidores urbanos. 

O projeto foi originalmente arquitetado e prototipado como um **aplicativo Android nativo em Kotlin com Jetpack Compose** (hospedado no repositório parceiro da equipe), focado em performance mobile e acessibilidade extrema. 

Para a **Atividade II da disciplina de Interfaces Digitais UX/UI**, a equipe desenvolveu esta **versão Front-End Web responsiva**, hospedada diretamente no **GitHub Pages**, permitindo que a banca examinadora, docentes e usuários finais possam navegar e validar o fluxo completo em tempo real a partir de qualquer navegador desktop ou smartphone, sem a necessidade de emuladores ou compilação local.

---

## 🎯 Pesquisa de UX e Personas Centrais

O desenvolvimento da interface partiu da coleta de dores reais e mapeamento de empatia com duas personas fundamentais:

* **Dona Maria (68 anos) — Consumidora Urbana:**  
  * *Dores:* Presbiopia severa, tremores motores leves e insegurança ao navegar em interfaces poluídas.  
  * *Solução UI:* Tipografia em grande escala, paleta com alto contraste (evitando cinzas claros), botões largos com alvos de toque generosos e atalhos rápidos com preenchimento assistido.
* **Seu José (54 anos) — Feirante e Produtor Rural:**  
  * *Dores:* Pouco tempo hábil durante a feira livre, ambiente com excesso de reflexo solar e aversão a cadastros complexos.  
  * *Solução UI:* Painel administrativo enxuto para adicionar colheitas do dia em 3 cliques e controle visual imediato para exclusão de itens esgotados.

---

## 🏗️ Atendimento às Diretrizes da Atividade II

### 1. Arquitetura de Componentes e Microsserviços na Interface
A interface não foi concebida como uma página estática acoplada. O front-end adota o padrão de **Microsserviços de Interface (Micro Front-ends / Módulos Independentes)**:
* **MicroservicoCatalogo:** Responsável exclusivamente pela gestão de estoque, listagem, filtros de colheita e metadados dos produtores.
* **MicroservicoCarrinho:** Responsável isoladamente pelas regras tributárias, taxas de frete/retirada, cálculo dinâmico de subtotal e checkout.
* **Independência Operacional:** Os módulos comunicam-se via contratos desacoplados de dados. Caso o serviço de checkout sofra indisponibilidade, o catálogo de colheitas permanece plenamente funcional e pesquisável pelo usuário.

### 2. Identidade Visual e Design System no Código
Centralização dos tokens de design nas variáveis de interface, garantindo consistência estrita:
* **Verde Primário (`#2E7D32`):** Conecta a identidade à terra, frescor e sustentabilidade ambiental.
* **Laranja CTA (`#E65100`):** Destinado estritamente aos botões de ação de alta conversão (Adicionar, Finalizar).
* **Superfície Suave (`#F9FBE7`):** Reduz a fadiga ocular em comparação ao branco puro (`#FFFFFF`).
* **Tipografia e Alvos:** Escala hierárquica legível e alvos de toque com altura mínima de **48px**, prevenindo toques acidentais.

### 3. Acessibilidade Prática no Código (WCAG 2.1 - Nível AA)
* **Semântica HTML5 Rigorosa:** Uso correto e sem concessões de `<header role="banner">`, `<nav aria-label="...">`, `<main role="main">`, `<section>`, `<article>` e `<footer role="contentinfo">`.
* **Navegabilidade 100% por Teclado (Tecla Tab):** Foco visível estilizado com anel contrastante (`outline: 3px solid #E65100; outline-offset: 2px`) em todos os elementos interativos.
* **Atributos ARIA:** Inclusão de `aria-label` descritivos em botões de ação e incremento/decremento, além de `aria-live="polite"` nos contêineres reativos para leitores de tela.
* **Contraste de Cores:** Supera os 4.5:1 exigidos pela norma, atingindo **16.1:1** no texto principal e **4.8:1** no botão de ação principal.

### 4. Responsividade Mobile-First
Layout fluido projetado com foco no uso em smartphones (formato compacto de fácil manuseio com o polegar), adaptando-se confortavelmente e de maneira centralizada a telas de tablets e computadores desktop.

---

## 📱 Fluxo de Navegação e Demonstração

Para facilitar a avaliação da banca, a tela inicial de autenticação disponibiliza **Atalhos Rápidos de Demonstração UX**:
1. **Persona 1: Dona Maria (Compradora):** Conduz imediatamente à vitrine de colheitas frescas, permite filtrar por categorias (Verduras, Frutas, Legumes, Tubérculos), adicionar itens à sacola e simular a alternância entre retirada grátis e entrega ecológica (+ R$ 5,00).
2. **Persona 2: Seu José (Feirante):** Acessa a área administrativa, permitindo cadastrar um novo alimento no catálogo da feira e excluir produtos em tempo real.

---

## 🔗 Links Relevantes
* 🌐 **Aplicação Web Ativa (GitHub Pages):** [[suspicious link removed]]([suspicious link removed])
* 📦 **Repositório da Versão Mobile Nativa (Android/Kotlin):** [feiralocal-android]([suspicious link removed])

```

---
