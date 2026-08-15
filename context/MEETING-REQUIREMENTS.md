# Requisitos da reunião (2026-08-14, 2h47min) — 12-11x-frontier vira o design principal

Transcrito com whisper (large-v3-turbo, GPU) sobre `/home/eder/2026-08-14 17-05-59.mp4`.
Lido na íntegra (1660 segmentos). O que segue é o que foi realmente dito, não inferido.

## Decisão estrutural

- **`12-11x-frontier` deixa de ser uma de 16 direções concorrentes e vira O design
  principal.** Confirmado explicitamente no fim da call: *"for the other websites we
  have the headphones, I'm gonna use the... x11... that's it."* (headphones = a foto do
  rep à noite que já é o hero atual do 12).
- **Codex CLI é o executor de design daqui pra frente**, não Claude direto.
- As outras 15 pastas ficam só como referência de elementos a reaproveitar pontualmente
  (ver "Elementos a importar" abaixo), não como design a manter.

## Por que o 12 venceu (razões ditas em voz alta, para não perder o motivo)

- *"we should be leaning more towards black and white... because these are all brown,
  it's all warm"* — rejeitaram as direções em tons quentes/bege (oyster, valley) porque
  a marca é azul: *"our thing is blue... it's a clash."*
- Evitar o laranja/creme que lembra a Claude/Anthropic: *"excitingcloud.com... it's
  because it's Claude's color."*
- Gostaram especificamente: a linha de herói "He's still nodding.", a seção de baixo com
  fotos de pessoas reais (o carousel), a tabela de comparação simples, o marquee com os
  nomes das funcionalidades (HumanCue™, Buyer Readiness Index™ etc — já existe no 12,
  mantém como está).

## Paleta de marca confirmada

*"there's like a reference because our entire website has this blue to cyan and to
green. So this would be the palette that we are using. A little cyan, a little blue, a
little gray."* — ciano, azul, cinza. Nada de marrom/bege/creme quente.

## Fonte: Satoshi

Escolhida ao vivo depois de revisar fontshare.com ("considered one of the best black and
white sites"). Testaram light/regular/medium — preferiram **light, mais fina** para o
headline gigante do hero. Fonte não está no Google Fonts; está em fontshare.com (grátis,
auto-hospedável) — baixar de lá, não usar substituto sem checar se dá pra usar a real
primeiro.

## HERO — substituição completa, já decidida e testada ao vivo

Processo real: geraram a banda de pessoas por IA, testaram dezenas de variações de
posição/quebra de linha/peso/cor do texto sobre a imagem, adicionaram gradiente escuro
por trás do texto pra letra não se perder na roupa das pessoas, centralizaram, desceram
as pessoas pra sobrar espaço em branco em cima. Confirmação final literal: *"so I guess
that's it, that's gonna be the hero."*

**As duas imagens em `site/assets/hero-mockup-reference.png` e `hero-people-band.png`
são o resultado real dessa decisão — usar como estão, não redesenhar do zero.**

- Fundo branco, nav azul-marinho, logo com anel ciano
- Headline em duas linhas: "We know" (peso mais leve) / "what you're thinking." (peso
  bold, ponto final em ciano)
- Subheadline: mantém a linha já usada no site — *"Conversion intelligence tells you
  what the buyer said. PitchGenius tells you what to say next."*
- Botões do nav: "See the live call" (ghost) + "Book a pilot" (navy sólido) — já existe
  essa estrutura no 12, só precisa da variante clara
- Banda de 8 retratos P&B, corte na altura do peito, ombro a ombro — `hero-people-band.png`
- **Isso é um ponto de partida, não o fim**: *"we'll just go find more pictures once you
  get the color base."* Mais fotos vêm depois; não travar o layout de um jeito que só
  funciona com exatamente essas 8 pessoas.

## Buyer Blueprint — nova paleta (arquivo já pronto: `buyer-blueprint-palette.json`)

Confirmado ao vivo, cor por cor, nessa mesma call (é literalmente a gravação dessa
iteração). Aplicar os hex exatos do JSON:
- fundo `#EBF3FA`, borda `#0052CC`
- roda DISC colorida por eixo, todas as letras em negrito (16px/700), não só a
  selecionada — pedido explícito: *"can you make the other ones bold too?"*
- Trust Triggers™ verde, Resistance Signals™ vermelho
- nova seção **"Missing evidence"** com botão "Add evidence" — não existe no card atual,
  precisa ser adicionada
- exemplo de perfil mudou pra "Skeptical Profit-Driven Analyst" — **incerto se isso é
  conteúdo definitivo ou só um exemplo usado durante o teste de cor**; a call não
  explica a troca. Manter Judd Barakove como dado real do produto em todo o resto do
  site (PRODUCT.md) a menos que uma instrução futura confirme a troca definitiva.

## Buyer Readiness / post-call — redesenho completo (arquivo já pronto: `buyer-readiness-palette.json`)

Não é recolor, é estrutura nova:
- container branco, `border-radius:16px`, fundo externo `#F0F4F8`
- heading principal em negrito (leitura do vendedor sobre o comprador)
- score label, bloco de citação com borda esquerda rust `#C2410C`
- "CRM says: [estágio]"
- **caixa "BLOCKED" nova** — rosa claro, borda vermelha, título vermelho, bullets em
  bordô, listando as objeções reais do comprador
- link colapsável "Transcript this diagnosis was read from"
- **badge de confiança da IA, novo** — anel circular verde sobre trilho cinza, texto
  central "High", label "AI confidence" — elemento que não existe hoje, precisa ser
  criado do zero
- personagem de exemplo "Gerald" — mesma ressalva do Blueprint acima, incerto se é
  definitivo.

## Seções escuras — varredura geral, não só os dois cards

Pedido repetido e genérico, não específico a um único elemento: *"just wherever those
big dark ones do the same thing... where else is that big dark ugly one"* — testaram
inverter uma seção preta pra branca com texto preto e gostaram do resultado. **Aplicar
esse mesmo tratamento em toda seção escura pesada do 12** (a seção sticky-pin com foto
de fundo escura, por exemplo), não só nos dois cards já mapeados — usar julgamento, mas
o padrão pedido é: menos preto sólido, mais branco/cinza-claro com acento de cor.

## Elementos a importar de outras direções (já descartadas como página, não como ideia)

- **"Flip cards"** — efeito de virar card pra mostrar antes/depois (pré-call / pós-call).
  Gostaram bastante: *"the main functionality thing that was cool was the flip cards...
  it's almost like pre-call, post-call."* Vale considerar como interação nos moment
  cards do 12.
- Tabela de comparação simples (já bate com o que o 12 tem — manter como está, só
  confirmar que não ficou "under the column", ou seja, cada linha lado a lado, não uma
  coluna isolada).

## Fora de escopo desta reunião (não confundir com pedido de landing page)

A primeira ~30min da call é sobre integração de API/enriquecimento de dados
(ZoomInfo, GTM, client id/secret, permissões OAuth) — é conversa de backend/parceria de
negócio, não pedido de mudança na landing page. Ignorar para efeito de design.
SEO/AEO também foi citado como tarefa separada, posterior.

## Posicionamento do produto (contexto, não uma tarefa de copy explícita)

Frase forte sobre a voz do HumanCue™, potencialmente útil pra copy futura: *"it's not a
teleprompter... I'm here to give you the buyer signal, next best move, best thing to
say, and move on — and I stay silent when it's time to be silent and let you do your
work."* Considerar se algum trecho do site deveria adotar essa voz em primeira pessoa,
mas não foi pedido como tarefa concreta nesta call — registrar, não implementar sem
confirmação.
