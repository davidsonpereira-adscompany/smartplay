# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML/CSS/JS em arquivo único por página (incumbente; publicado via GitHub Pages). Tipografia Montserrat obrigatória. Sem frameworks.

## Users

Famílias brasileiras classe C/D, 25–50 anos, que querem substituir TV a cabo por algo mais barato. Perfis: pai/mãe que decide a assinatura da casa; apaixonados por futebol; quem já assina streaming e sente falta de canal ao vivo; moradores de zonas rurais com internet leve (rádio/chip). Decisão acontece no celular, frequentemente à noite, e fecha pelo WhatsApp.

## Product Purpose

Smart Play é um serviço IPTV: +200 canais ao vivo, filmes, séries, esportes, novelas, infantil e animes em HD/4K, no app próprio (Smart TV, celular, computador, tablet, TV Box, Fire Stick, Chromecast). Sucesso da página = o visitante iniciar conversa no WhatsApp — prioridade nº 1: pedir o teste grátis de 2 horas; nº 2: assinar um plano.

## Positioning

"A família inteira assistindo." — até 3 telas simultâneas por uma fração do preço da TV a cabo (entrada R$16,90), sem fidelidade, com suporte humano via WhatsApp e sinal que funciona até em internet leve de zona rural. A qualidade de vídeo se ajusta sozinha à conexão (não há ajuste manual).

## Operating Context

- Venda 100% via WhatsApp: 5516982156332. Cada botão envia mensagem percent-encoded única que identifica a origem do clique (plano+preço, teste por seção, instalação, dúvida, rodapé). Isso é infraestrutura de rastreamento e não pode ser alterado.
- Páginas publicadas no GitHub Pages (repo davidsonpereira-adscompany/smartplay).
- V1 (`03-FUNIL-VENDAS/pagina-de-vendas-smart-play.html`) e V2 (`...-v2.html`) permanecem ativas; V3 é protótipo de avaliação — o usuário decide depois se substitui.

## Capabilities and Constraints

- Planos: 15 dias R$16,90 (1 tela) / Mensal R$28,00 (1 tela) / Bimestral R$52,90 (2 telas) / Trimestral R$77,90 (3 telas, "Mais Popular") / Semestral R$147,90 (3 telas) / Anual R$267,90 (3 telas, "Melhor Custo-Benefício"). Todos sem fidelidade. Nunca dizer que o máximo é 2 telas — é "até 3 telas" (a partir do trimestral).
- Teste grátis de 2 horas existe e é a porta de entrada.
- Requisito técnico: ~10 MB de internet; funciona com internet via rádio/chip; atualização automática semanal.
- Nicho sensível a linguagem de anúncio: comunicação direta ao consumidor, sem promessas indevidas.
- Regras duras: acentuação impecável; emojis em URLs de WhatsApp sempre percent-encoded; responsivo obrigatório (480/768/1024/desktop); nenhuma menção a IA/ferramentas em nenhum output.

## Brand Commitments

- Big Idea: "A família inteira assistindo." (pai na sala, mãe no quarto, filho no celular — ao mesmo tempo).
- Paleta Coral Família (vinculante, confirmada pelo usuário para a V3): coral #FF6B6B, dourado CTA #FFD93D, ciano #4ECDC4, base escura #0F0808. Tipografia Montserrat (inegociável).
- Logo: badge circular com anel coral, play interno, ponto dourado; wordmark "SmartPlay" + rótulo "ENTRETENIMENTO" em ciano. PNG em `assets/logo-smartplay-1080.png`.
- Tom: linguagem de resultado (o que a família ganha), nunca de recurso técnico.

## Evidence on Hand

- 12 depoimentos com fotos de perfil (`03-FUNIL-VENDAS/img/avatars/av01–av12.jpg`) — conteúdo ilustrativo aprovado pelo usuário; preservar como está.
- Vitrines 1096×600 com capas reais atuais (`img/categories/mosaico-*.png`): filmes, séries, esportes, novelas, infantil, animes.
- 12 capas oficiais individuais (`img/capas/`), 21 posters (`img/posters/`), 18 logos SVG de canais (`img/logos/`).
- 7 imagens 3D de dispositivos com fundo transparente (`img/devices/*-3d.png`).
- Foto hero: família no sofá assistindo futebol (`img/hero/familia-hero.jpg`).
- Vídeos locais do carrossel (`img/videos/`): replay, esportes, barra (.webm/.mp4).
- Não existem: métricas públicas, prêmios, imprensa — não inventar.

## Product Principles

1. O WhatsApp é o caixa: toda decisão de design serve a iniciar conversa — teste grátis primeiro, plano depois.
2. Mostrar a família assistindo vale mais que descrever tecnologia; conteúdo reconhecível (capas, futebol, novela) é o argumento.
3. Preço é força, não vergonha: R$16,90 e "sem fidelidade" merecem destaque de vitrine.
4. Funciona no celular fraco: página leve, imagens locais otimizadas, nada que dependa de CDN de terceiros.
5. Confiança pelo concreto: telas, prazos e valores exatos — nunca superlativo vazio.

## Accessibility & Inclusion

Público majoritariamente mobile e de conexões lentas: peso de página e legibilidade em telas pequenas têm prioridade. Contraste adequado sobre fundo escuro.
