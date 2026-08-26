---
name: Smart Play — A Sala à Noite
description: Mundo visual V3 da página de vendas — a noite de TV da família, iluminada pela luz da própria tela.
colors:
  breu: "#090404"
  noite: "#0F0808"
  luz-coral: "#FF6B6B"
  luz-ciano: "#4ECDC4"
  luz-ouro: "#FFD93D"
  texto: "#EFDEDE"
  texto2: "#C9A6A6"
  texto-dim: "#A07E7E"
  oncta: "#2B1608"
typography:
  display:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "clamp(38px, 6.4vw, 76px)"
    fontWeight: 900
    lineHeight: 1.02
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "clamp(30px, 4.6vw, 52px)"
    fontWeight: 800
    lineHeight: 1.08
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: 1.6
  body:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "16px"
    fontWeight: 300
    lineHeight: 1.75
  label:
    fontFamily: "Montserrat, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    letterSpacing: "0.22em"
rounded:
  gc: "5px"
  sm: "6px"
  md: "8px"
  lg: "14px"
  xl: "16px"
  pill: "999px"
spacing:
  container-x: "32px"
  container-x-mobile: "20px"
  secao-topo: "110px"
  secao-base: "90px"
  secao-topo-mobile: "76px"
  titulo-apos-hora: "14px"
  fala-apos-titulo: "18px"
  botoes-apos-fala: "34px"
  conteudo-apos-fala: "44px"
components:
  botao-ligar:
    backgroundColor: "{colors.luz-ouro}"
    textColor: "{colors.oncta}"
    rounded: "{rounded.pill}"
    padding: "18px 36px"
  botao-quieto:
    backgroundColor: "rgba(255,255,255,0.03)"
    textColor: "{colors.texto}"
    rounded: "{rounded.pill}"
    padding: "18px 28px"
  botao-quieto-hover:
    backgroundColor: "rgba(255,255,255,0.06)"
  plano-ir:
    textColor: "{colors.texto}"
    rounded: "{rounded.pill}"
    padding: "12px 24px"
  gc-transmissao:
    backgroundColor: "rgba(9,4,4,0.62)"
    textColor: "#FFFFFF"
    rounded: "{rounded.gc}"
    padding: "8px 15px"
  marca-acao:
    backgroundColor: "{colors.luz-ouro}"
    textColor: "{colors.oncta}"
    rounded: "{rounded.pill}"
    padding: "11px 22px"
---

# Design System: Smart Play — A Sala à Noite

> **Escopo.** Este documento descreve o mundo visual **V3 "A Sala à Noite"** (seed `a1cfe3ce`), construído em `03-FUNIL-VENDAS/pagina-de-vendas-smart-play-v3.html`. É uma identidade substituta que hoje existe **apenas na página V3**. As páginas V1 e V2 (`pagina-de-vendas-smart-play.html` e `...-v2.html`) permanecem no visual incumbente anterior e **não** seguem este documento.

## Overview

**Creative North Star: "A Sala à Noite"**

A página não descreve o produto — ela **é** a sala da família à noite. Cada seção é um cômodo em um momento da noite de TV (o jogo às 20:15, a novela às 21:30, a maratona às 23:40, a conta às 23:58, a casa dormindo às 00:52), e a única fonte de luz de cada cômodo é a própria tela. O fundo é breu quase absoluto (#090404); tudo que se destaca, destaca-se porque está **iluminado**, não porque está emoldurado. O mundo recusa deliberadamente o padrão hero + grid de cards da categoria streaming: não há cards, não há bordas estruturais, não há caixas — há luz coral, ciano e dourada banhando títulos, telas e botões.

A narrativa é cronológica e doméstica: o visitante se reconhece na cena (a foto real da família no sofá, com a luz da TV tremulando), percorre a própria noite momento a momento, vê a conta da noite (planos como um extrato iluminado, não como cards de preço) e, no fim, "liga a TV" da casa dele — o teste grátis de 2 horas no WhatsApp. O dourado é o botão de ligar do controle remoto: é a única cor de ação.

**Key Characteristics:**
- Fundo breu (#090404/#0F0808) com hierarquia construída por iluminação, nunca por bordas ou cards.
- Uma variável `--glow` por seção (coral, ciano ou ouro) governa título, divisor, GC e sombra daquele cômodo.
- Rótulos de hora ("22:47 · TV DA SALA") e GC de transmissão sobre as imagens, como legendas de TV ao vivo.
- Montserrat em todos os pesos (300 a 900); horas e preços sempre em dígitos tabulares.
- Movimento de televisão: luz que tremula, canal que troca, seções que "acendem" ao entrar na tela.

## Colors

Uma paleta de escuridão quente com três luzes de tela: coral, ciano e ouro — cada seção acesa por uma delas.

### Primary
- **Luz Coral** (#FF6B6B): a luz principal da casa. Cor da marca (anel e play do logo), do ponto "AO VIVO", do glow das seções Novela, Mensagens e Perguntas, do `em` de títulos coral, dos links dentro do texto e da moldura das fotos de depoimento. Usada também como cor de `::selection`.

### Secondary
- **Luz Ciano** (#4ECDC4): a luz fria da tela ligada. Glow das seções Jogo, Madrugada e Telas da Casa; luz tremulante sobre a foto do hero; rótulo "ENTRETENIMENTO" da marca; halo sob os dispositivos flutuantes; selo "Melhor custo-benefício".
- **Luz Ouro** (#FFD93D): a luz de ação — o botão de ligar. Fundo do `botao-ligar` e do `marca-acao`, ponto dourado do logo, preço em destaque no hero, plano em destaque (`aceso-max`), selos "Mais Popular", ícones de garantia, glow das seções Desenho, Conta e Fechamento, e o anel de foco (`:focus-visible`).

### Neutral
- **Breu** (#090404): o fundo da página inteira e a base dos véus/gradientes sobre a foto do hero.
- **Noite** (#0F0808): tom de base da paleta (theme-color do navegador); breu ligeiramente mais claro.
- **Texto Aceso** (#EFDEDE): texto padrão do corpo; branco aquecido pelo escuro da sala.
- **Texto Meia-Luz** (#C9A6A6): parágrafos de apoio (`.fala`), respostas do FAQ, textos de depoimento.
- **Texto Penumbra** (#A07E7E): notas, horários apagados, equivalências de preço, nomes de arroba.
- **Sobre o Ouro** (#2B1608): o marrom-escuro do texto que senta sobre qualquer superfície dourada (botões, selo do plano destacado).
- **#FFFFFF puro**: reservado a títulos, nomes e ao que está mais perto da luz.
- Divisores e contornos discretos usam branco translúcido: `rgba(255,255,255,0.06)` (linhas do extrato e rodapé), `0.07` (FAQ), `0.15–0.16` (contorno de botões quietos).

### Named Rules
**A Regra da Luz do Cômodo.** Cada seção declara um único `--glow` (coral, ciano ou ouro) inline no HTML, e esse valor governa tudo que brilha ali: o gradiente radial do teto (`.comodo::before`, 13% de opacidade), a cor do rótulo de hora e seu divisor, o `em` do título e seu text-shadow, o destaque do GC e a sombra colorida da tela. Nunca duas luzes no mesmo cômodo.

**A Regra do Ouro Único.** O dourado #FFD93D é ação e destaque máximo — botão de ligar, plano recomendado, foco de teclado. Ele nunca vira cor decorativa de fundo ou de texto corrido; sua raridade é o que faz o botão parecer o botão de ligar.

## Typography

**Display/Body Font:** Montserrat (com fallback `sans-serif`), pesos 300, 400, 500, 600, 700, 800, 900 + itálico 400, via Google Fonts.

**Character:** Uma única família em dois extremos: peso 900 apertado (letter-spacing negativo) para os títulos que gritam na sala escura, e peso 300 com entrelinha folgada (1.75) para a fala baixa dos parágrafos. O contraste de peso substitui o contraste de fonte.

### Hierarchy
- **Display** (900, clamp(38px, 6.4vw, 76px), lh 1.02, ls -0.03em): exclusivo do título do hero (`.sala-titulo`), branco puro com text-shadow escuro sobre a foto. No mobile: clamp(30px, 9.6vw, 42px).
- **Headline** (800, clamp(30px, 4.6vw, 52px), lh 1.08, ls -0.025em): título de cada cômodo (`.titulo`); branco com text-shadow de 60px na cor do `--glow`; a palavra de ênfase em `em` colorido pelo glow (nunca itálico — `font-style: normal`). A variante do fechamento (`.dorme-titulo`) sobe para 900 e clamp até 54px.
- **Title** (700, 17px): nome do plano no extrato; preço do plano em 800, clamp(24px, 3vw, 34px), tabular. Nomes de depoimento em 700, 14px.
- **Body** (300, 16–17px, lh 1.7–1.75): a "fala" de cada seção, limitada a 52–58ch; ênfases em `strong` 600 na cor do texto aceso ou branco. Respostas do FAQ em 14px, máx. 68ch.
- **Label** (600, 11.5–13px, ls 0.14–0.24em, tabular-nums): os rótulos de hora (`.hora`, `.gc-sala`, `.momento-gc`, `.dorme-hora`) e selos de plano (10.5px, 800, uppercase, ls 0.14em). É a voz de "legenda de transmissão" do sistema.

### Named Rules
**A Regra dos Dígitos Tabulares.** Toda hora (22:47, 00:12) e todo preço (R$16,90, R$0,93/dia) usa `font-variant-numeric: tabular-nums`. Números aqui são relógio e extrato — alinham como em um painel.

**A Regra da Ênfase Acesa.** Dentro de um título, a ênfase é sempre `em` sem itálico, colorido pelo `--glow` da seção. Dentro de um parágrafo, a ênfase é `strong` 600 mais claro que o texto ao redor. Nunca sublinhado, nunca caixa alta no corpo.

## Layout

Coluna única de leitura: container de **1140px** máximos com padding lateral de 32px (20px abaixo de 640px). Não há grid de página — a página é uma sequência vertical de "cômodos" (`section.comodo`), cada um respirando **110px acima / 90px abaixo** (100px nas seções Telas e Perguntas; 76px no topo em mobile). O hero ocupa **100svh** com o conteúdo ancorado embaixo (padding-bottom 76px) e a marca fixada no topo por posicionamento absoluto.

O ritmo interno de cada cômodo é fixo: hora → título (+14px) → fala (+18px) → conteúdo (tela/extrato/fita, +44–48px) → botões (+34px no hero). A cronologia das horas (22:47 → 20:15 → 21:30 → 08:00 → 23:40 → 23:58 → 00:12 → 00:24 → 00:31 → 00:52) é a espinha da página.

Três padrões de largura quebram a coluna: o **duo de telas** (grid 1fr 1fr, gap 22px; empilha em 1 coluna abaixo de 900px), as **fitas horizontais** (depoimentos, dispositivos e estante de capas, que sangram além do container com máscara de fade nas bordas) e o **FAQ**, que estreita para 780px.

**Responsivo:** breakpoints em **900px** (duo empilha; extrato de planos reorganiza para 2 colunas com o botão ocupando 2 linhas) e **640px** (padding 20px, botões do hero e do fechamento em largura total, capas 190px, cartões de depoimento 290px, dispositivos 175px, preços 24px). `overflow-x: hidden` no body; as fitas roláveis escondem a barra de rolagem.

## Elevation & Depth

Não existem sombras de elevação de interface — **a profundidade é luz**. O sistema é plano sobre breu e usa três mecanismos: (1) o **glow do teto** de cada cômodo (gradiente radial de 13% do `--glow` descendo do topo da seção), (2) **sombras coloridas de tela ligada** (`0 0 90px` no `--glow` a 16%, somado a uma sombra preta grande `0 30px 80px rgba(0,0,0,.55)` que assenta as vitrines no escuro) e (3) **halos pontuais** (o botão dourado com `0 6px 40px rgba(255,217,61,0.28)`, o ponto AO VIVO com `0 0 10px` coral, o ponto do logo com `0 0 8px` ouro, o halo ciano difuso sob cada dispositivo flutuante).

Superfícies "elevadas" sem imagem usam translucidez, não sombra: os GCs assentam em `rgba(9,4,4,0.55–0.62)` com `backdrop-filter: blur(6–8px)`; cartões de depoimento e botões quietos usam branco a 2,5–3%.

### Shadow Vocabulary
- **Tela ligada** (`box-shadow: 0 30px 80px rgba(0,0,0,.55), 0 0 90px color-mix(in srgb, var(--glow) 16%, transparent)`): toda vitrine de conteúdo (`.momento-tela`).
- **Botão de ligar** (`box-shadow: 0 6px 40px rgba(255,217,61,0.28), 0 2px 10px rgba(0,0,0,.5)`; hover sobe para `0 10px 56px` a 0.42): exclusiva do CTA dourado.
- **Capa na estante** (`box-shadow: 0 18px 44px rgba(0,0,0,.6)`): posters do catálogo.
- **Dispositivo no ar** (`filter: drop-shadow(0 24px 28px rgba(0,0,0,.6))` + halo ciano radial no chão): imagens 3D de aparelhos.

### Named Rules
**A Regra Zero Bordas, Zero Cards.** Nada na página é um card com borda e fundo de caixa. Hierarquia e agrupamento vêm de iluminação, translucidez e linhas divisórias de 1px em branco a 6–7%. Se um bloco novo precisar "se destacar", ele recebe luz — não moldura.

## Shapes

Formas de tela e de controle remoto. As **vitrines de conteúdo** têm cantos de 14px; capas de catálogo, 8px; cartões de depoimento, 16px; GCs de transmissão, 5–6px (o canto mais reto do sistema, como um lower-third de TV). Todos os **botões são pílulas** (999px) — inclusive o "Escolher" do extrato — e todos os elementos da marca são **círculos** (anel de 38px com traço coral de 2.5px, play interno, ponto dourado). O extrato de planos e o FAQ não têm forma própria: são listas separadas por linhas de 1px. As fitas horizontais terminam em **máscara de fade** (`mask-image` linear, 3–7% nas bordas), nunca em corte seco.

## Components

### Botões
- **Shape:** pílula (border-radius 999px) em todos os casos.
- **`botao-ligar` (primário, "o botão de ligar do controle"):** fundo ouro #FFD93D, texto #2B1608 em 800/15px, padding 18px 36px, ícone SVG de power de 18px à esquerda, sombra-halo dourada. Hover: sobe 2px (`translateY(-2px)`) e o halo cresce. Sempre leva o WhatsApp do teste grátis. Existe em duas encarnações: nos botões do hero/fechamento e, menor (700/13px, padding 11px 22px), como `marca-acao` no canto da marca.
- **`botao-quieto` (secundário):** fantasma sobre o breu — fundo branco a 3%, contorno 1px branco a 16%, texto #EFDEDE 600/14px, padding 18px 28px. Hover: contorno a 34%, fundo a 6%. Usado para a ação alternativa (assinar, rever planos, instalar, testar depois dos preços).
- **`plano-ir` ("Escolher"):** pílula de contorno, 700/13px, padding 12px 24px. Hover: contorno e texto viram ouro. No plano destacado (`aceso-max`) ele já nasce dourado sólido com halo.
- **Foco:** todo elemento focável recebe `outline: 2px solid #FFD93D` com offset de 3px.

### GC de transmissão (hora · lugar) — componente-assinatura
O rótulo que transforma imagem em transmissão. Duas formas:
- **`gc-sala` (hero):** "AO VIVO 22:47 · TV DA SALA · FUTEBOL" — 12px/600, tracking 0.16em, tabular; fundo `rgba(9,4,4,0.55)` com blur 8px, raio 6px, padding 9px 18px. O "AO VIVO" em 800 branco com ponto coral pulsante (animação `pulsa`, 2.2s).
- **`momento-gc` (sobre as vitrines):** canto inferior esquerdo da imagem (18px/16px), 11.5px, raio 5px, fundo a 62% com blur 6px; a primeira palavra em `b` 800 colorida por `color-mix` do `--glow` com branco.
- **`hora` (fora de imagem):** o mesmo idioma sem caixa — 13px/600, tracking 0.22em, cor `color-mix(72% do --glow + texto)`, seguido de um traço-divisor de 64px em gradiente do glow para transparente.

### Extrato de planos (a conta da noite)
Os 6 planos **não são cards**: são linhas de um extrato. Cada `.plano` é um grid de 4 colunas (nome+telas / preço / equivalência / botão) com 26px de padding vertical, separado por linhas de 1px branco a 6%. Preço em 800 tabular clamp(24–34px); equivalência ("R$25,97 por mês") em 12.5px penumbra; hover acende a linha com branco a 2%. O plano recomendado (`aceso-max`, Trimestral) é a **linha acesa**: gradiente dourado a 6% varrendo da esquerda, bordas superior/inferior douradas a 28%, preço ouro com glow, botão dourado sólido e selo "MAIS POPULAR" (10.5px/800, uppercase, tracking 0.14em). O selo ciano marca o Anual. Abaixo de 900px o grid vira 2 colunas com o botão à direita ocupando as duas linhas.

### Fitas (tickers)
Três esteiras infinitas com conteúdo duplicado via script e translateX de 0 a -50%:
- **Mensagens da madrugada** (depoimentos): duas fitas em direções opostas (85s e 97s reverse, linear), com máscara de fade 7%. Cada `.msg` é um cartão de 330px (290px mobile) e raio 16px **sem borda** — fundo em gradiente radial coral a 7% sobre branco a 2,5%; foto redonda de 42px com anel coral a 35%, nome + selo de verificado ciano, arroba penumbra, ícone de rede no canto, citação `@smartplay` em coral 600. Hover: pausa a fita e o cartão sobe 3px.
- **Telas da casa** (dispositivos): fita única de 34s, itens de 235px (175px mobile) com imagem 3D flutuando (animação `flutua`) sobre halo ciano.
- **Estante da madrugada** (capas): não anima — rola por toque/scroll (scrollbar oculta), capas de 240px de altura (190px mobile), raio 8px, hover sobe 8px, fade de 3% nas bordas.

### FAQ (perguntas no escuro)
Acordeão de lista sem caixas: linhas de 1px branco a 7%, pergunta em 600/15.5px, chevron penumbra que gira 180° e acende em coral ao abrir. Abertura animada por `grid-template-rows: 0fr → 1fr` (0.4s). Comportamento exclusivo: abrir uma pergunta fecha as demais; `aria-expanded` sincronizado via script.

### Marca
Reconstrução em CSS do badge: anel de 38px com traço coral 2.5px, círculo-play coral de 21px com triângulo SVG branco, ponto dourado de 7px com glow no canto inferior direito; wordmark "SmartPlay" 800/21px branco + "ENTRETENIMENTO" 600/7px uppercase tracking 0.35em em ciano. No rodapé, a mesma marca com opacidade reduzida (anel a 60%, textos apagados).

### Movimento (gramática)
O movimento é sempre **comportamento de televisão**, nunca ornamento:
- **`tvFlicker`** (7s, ease-in-out, infinita): a luz ciano sobre a foto do hero tremula em opacidade (0.78–1) com batidas irregulares, como uma TV ligada refletindo na sala.
- **Troca de canal** (`trocaCanal`, 12s): a última palavra do título do hero rola verticalmente entre "o jogo. / a novela. / o desenho. / tudo junto." em passos de 1.1em, em ouro.
- **Ignição por seção:** cada `.comodo` entra apagado; um IntersectionObserver (threshold 0.18) aplica `.aceso`, que acende o glow do teto em 1.6s e revela os filhos `.surge` (fade + subida de 26px, 0.9s, `cubic-bezier(.16,1,.3,1)`, escalonados em 0 / 0.08s / 0.16s). O hero já nasce aceso. Sem IntersectionObserver, tudo nasce aceso.
- **`flutua`** (5.5s): dispositivos sobem e descem 11px, dessincronizados por delays negativos (-1.8s, -3.7s).
- **`pulsa`** (2.2s): o ponto AO VIVO respira.
- **Hovers:** sempre discretos — subir 1–8px, acender contorno, pausar fita. Transições de 0.3–0.35s.
- **`prefers-reduced-motion: reduce`:** desliga todas as animações e transições, força `.surge` e o glow visíveis e congela a troca de canal na primeira palavra ("o jogo.").

## Do's and Don'ts

### Do:
- **Do** declarar um único `--glow` por seção (coral #FF6B6B, ciano #4ECDC4 ou ouro #FFD93D) e deixar que ele governe hora, ênfase do título, text-shadow, GC e sombra da tela — é assim que uma seção nova entra no mundo.
- **Do** abrir toda seção com o rótulo de hora tabular ("00:24 · PELA CASA TODA") mantendo a cronologia da noite coerente.
- **Do** usar o dourado exclusivamente como ação/destaque máximo, com texto #2B1608 por cima, e manter o CTA primário sempre apontando para o teste grátis de 2h no WhatsApp (mensagens percent-encoded intactas — são rastreamento).
- **Do** colocar GC de transmissão (fundo `rgba(9,4,4,0.62)` + blur) sobre toda imagem de conteúdo, e encerrar fitas horizontais com máscara de fade.
- **Do** escrever preços e horas em `tabular-nums`, ênfases de título em `em` colorido sem itálico, e manter Montserrat como única família.
- **Do** fornecer o caminho sem movimento: `prefers-reduced-motion` neutraliza tudo e o conteúdo continua completo e legível.

### Don't:
- **Don't** criar cards com borda e fundo de caixa, nem grids de cards de preço — planos são linhas de extrato, destaque é linha acesa, agrupamento é luz.
- **Don't** misturar duas cores de glow no mesmo cômodo, nem usar coral/ciano como cor de botão primário.
- **Don't** usar branco puro em texto corrido (reservado a títulos e nomes) nem fundos mais claros que os translúcidos de 2–6% sobre o breu.
- **Don't** aplicar este mundo às páginas V1/V2 sem decisão explícita — ele é, por ora, exclusivo da V3.
- **Don't** trocar as pílulas dos botões por cantos retos, nem adicionar sombras de elevação cinza-neutras — profundidade aqui é sombra preta + glow colorido.
