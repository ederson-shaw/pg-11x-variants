# O que foi dito sobre CADA uma das 16 páginas (reconstrução com prova, não memória)

Método: MEETING-REQUIREMENTS.md (já existente) resumia só a decisão final. Isso aqui é
a varredura pedida — projeto por projeto, na ordem real em que foram revisados — feita
comparando o ÁUDIO (whisper, timestamps) com FRAMES reais do vídeo `2026-08-14 17-05-59.mp4`
(a barra de URL do navegador, extraída quadro a quadro com ffmpeg) porque o áudio sozinho
é ambíguo (números soltos: "isso é o oito", "isso é o nove" — sem o vídeo eu estaria
adivinhando qual pasta era qual). Toda linha abaixo tem timestamp real do vídeo.

Existem DUAS passadas no vídeo: uma primeira revisão rápida (01:12:35–01:19:35, decisão
mantém/descarta) e uma segunda passada de reconferência (01:23:30–01:27:00, procurando uma
feature específica que não lembravam de onde vinha). Uma nota: 04-attio-producttruth nunca
foi aberta em nenhuma das duas passadas — não há registro de feedback sobre ela.

## 01-apollo-motion — 01:12:35–01:12:50 (1ª passada), 01:18:10–01:18:16 (2ª)
"it's using this font is very different" — reparo na fonte, sem elogio.
Decisão final (01:18:16): **"let's dump it, okay so we have two and close it"** — DESCARTADA,
junto com a 02.

## 02-polar-sticky — 01:12:50–01:13:29 (1ª), revisitada 01:17:50/01:18:00/01:26:20 (2ª)
"conversation intelligence... for the reps in the room, for the manager" — leram o copy.
"there's some images but they are not cropping cropping cropping" — reclamação: os retratos
das pessoas não cortam bem (mesmo bug de enquadramento que corrigimos nos 16 antes desta call).
Decisão final: **descartada junto com a 01** ("we have two and close it").

## 03-clay-system — 01:12:55–01:13:30 (1ª), revisitada 01:17:40 (2ª)
"the only problem is like the backgrounds... I would just delete it this hero" — a imagem de
fundo do hero foi chamada de "striking" (chamativa) mas ELE queria removê-la.
Segunda passada (01:17:46): **"I also close it a couple things I liked about it, but I like
those blocks people nice, I like the bottom half look more than..."** — gostou dos blocos/pessoas
e da metade de baixo do layout, mas fechou (descartou) mesmo assim.

## 05-oyster-handmade — 01:13:35–01:14:55 (1ª, a mais longa da 1ª passada), revisitada 01:17:30/01:19:35–01:20:15 (2ª)
**Fonte confirmada dos flip cards**: "the main functionality thing that was cool was the flip
cards... it's almost like pre-call, post-call" (01:14:45) — dito enquanto a URL mostrava
`05-oyster-handmade`, não outra página. MEETING-REQUIREMENTS.md já registrava "flip cards"
como elemento a importar mas não a origem — agora está confirmada.
01:16:17 confirma de novo: **"just the cards from the five"** = os cards do projeto 5 (oyster).
Screenshot tirado com FireShot (01:19:40) para arquivar antes de descartar a página como um
todo (a página 05 foi descartada como PÁGINA, só os flip cards foram levados adiante — já
diz isso o MEETING-REQUIREMENTS.md: "já descartadas como página, não como ideia").
STATUS: já implementado em 12-11x-frontier (Buyer Blueprint e Buyer Readiness ambos com
flip card funcional, testado por clique real nesta sessão).

## 06-slite-quiet — 01:14:55–01:15:20 (1ª), revisitada 01:17:25 (2ª)
Passagem rápida, sem elogio específico registrado.
Decisão final (01:17:29): **"we don't like six"** — DESCARTADA.
(Nota: confundiram "06-slite" com a palavra "slide" no áudio — "that's not slide one right"
— confirmado pelo vídeo que era mesmo a página 06, não outra.)

## 07-cursor-livedemo — 01:15:20–01:17:20 (1ª, a MAIS longa de toda a revisão), revisitada 01:24:23–01:24:45 (2ª, incluindo checar cursor.com de verdade)
Muito tempo de discussão, mista:
- 01:16:02 **"there's a lot to like about this one, this really is a lot to like about this one"**
- 01:16:09 confirma o número: **"this is the seven... you like it the animations"** — os
  elogios são às ANIMAÇÕES desta página.
- 01:16:33 problema apontado: **"you can't have the HumanCue on top of the hero picture very
  top"** — o card do produto sobrepondo a foto do hero no topo não funcionava.
- Na 2ª passada (01:24:23) eles chegam a abrir `cursor.com` de verdade no Google para
  comparar com a referência original, depois voltam pra 07 — não fica registrado um veredito
  final claro de manter/descartar; ficou em aberto ("we already passed through, oh we already
  dumped it, all right yeah, no, we keep it again, we kept it").
STATUS: incerto se algo específico desta página ainda falta portar — as animações elogiadas
não foram nomeadas com detalhe suficiente pra agir sobre elas com segurança.

## 08-eleven-clean — 01:16:55 (toque rápido, 1ª), 01:18:25–01:18:35 (2ª, decisão)
01:18:26: **"this is the eight and I don't know, it's just white text... dump it dump it"**
— DESCARTADA, crítica pontual: texto branco sem contraste/hierarquia.

## 09-hyperbound-ramp — 01:18:35–01:19:35 (a mais longa depois da 07)
**Fonte confirmada da tabela de comparação**: 01:18:37 "this is nine, we have images and the
barcode... this go with me I like this... the competitive thing that's nice, how to say it is
very very simple to compare, **not under the column**" — dito enquanto a URL mostrava
`09-hyperbound-ramp`. MEETING-REQUIREMENTS.md já citava a frase "not under the column" mas
não a origem — confirmada agora como sendo esta página, não a 12 original.
Também mencionaram: "the footer, ever close contract" e "the only thing that's good is
having the competitive comparison, I can take a screenshot" — ou seja, SÓ a tabela foi
aproveitada, o resto da página não.
STATUS: já implementado em 12-11x-frontier (tabela comparativa Gong/Clari/Chorus/
Salesforce/PitchGenius, linhas lado a lado — confirmado por screenshot nesta sessão).

## 10-unify-people — 01:20:25–01:21:45
**Fonte confirmada da decisão "preto e branco, não bege/marrom"**: 01:21:26 "I like this
human slide too... using some of those black and whites, because I think we should be
leaning more towards black and white... because these are all brown, it's all warm" — dito
com a URL em `10-unify-people`. Esta é a citação que já estava em MEETING-REQUIREMENTS.md,
mas agora está confirmado que o gatilho foi literalmente estar olhando pra esta página.
Decisão: **"I'm gonna keep that open for now"** — mantida em aberto, não formalmente
descartada nem escolhida como base.

## 11-gong-displace — 01:21:50–01:22:00
Passagem curta e crítica: **"I don't know what the animation is wrong, there's a lot"** —
problema com a animação, sem elogio registrado.

## 12-11x-frontier — 01:22:05–01:22:20
**"he's still nodding, this is the frontier, the one, and the first thing that I like the
best... I think it's great"** — confirma que a linha de herói "He's still nodding." foi o
motivo do 12 ter sido escolhido como base, ANTES mesmo da decisão final registrada no fim
da call (02:46:08). "and it's just getting a better hero line there" — ou seja, já estava
claramente na frente desde a primeira passada.

## 13-ashby-manifesto — 01:22:25–01:22:41
"now I have placed down on the date measure... the table, beginners still at the bottom,
nothing... I like the **signature**, signature... but I'm gonna dump it, okay, this is black,
so dark"
DESCARTADA por ser escura demais, MAS: gostou de algo chamado "signature" (sem mais detalhe
— não fica claro se é uma seção "assinatura"/selo de autenticidade, uma citação assinada, ou
outra coisa). **Não implementado em 12-11x-frontier porque não dá pra saber com segurança o
que é — fica em aberto, não vou inventar um formato pra isso.**

## 14-modal-technical — 01:22:41–~01:24:15 (a mais discutida depois da 07 e 09)
Elogio forte e repetido: "I love this thing, these really cool, but like you go above it,
yeah with these lines... the movement this way of the people" — gostaram do estilo de linhas/
diagrama técnico e um efeito de movimento com pessoas.
**Aqui é onde tentam (sem sucesso nesta seção) lembrar de onde vem o marquee de nomes de
funcionalidades**: "it was saying buyer blueprint, humancue... it's almost feeling like...
it's just scrolling the names of all the things, functionalities" — mencionado enquanto
olhavam pra 14, mas a frase seguinte ("I think it's on another website, I don't know the
name") mostra que ELES MESMOS não tinham certeza se o marquee era da 14 ou de outra —
dispara uma busca confusa de ~5 minutos (14→cursor.com→07→06→05→02→03→01→08) que não chega
a uma conclusão registrada no áudio.
STATUS: o marquee já existe em 12-11x-frontier (HumanCue™ · Buyer Readiness Index™ · Trust
Triggers™ · Resistance Signals™ · ...). A origem exata (14 ou outra) não foi confirmada por
eles mesmos no áudio, então não afirmo qual página originou — só que o resultado final já
está implementado.

## 15-mercury-executive — visitada rapidamente durante a busca confusa (01:25:40–01:25:55)
Sem comentário específico capturado nesta janela.
Possível referência indireta em 01:33:32–01:34:27 (sem confirmação de página): "this is a
very professional elegant site... but the problem is they're all both brown hues... it looks
very old money, like super rich people, beige, and royal blue" — elogiada estéticamente
("elegante") mas function como outro exemplo de "warm/brown" rejeitado pela decisão de ir
pro preto-e-branco. Não tenho certeza de que esta citação é sobre a 15 especificamente
(a URL não foi capturada no frame exato desta fala) — marco como não confirmado.

## 16-valley-watercolor — visitada 01:25:10–01:25:20 e 01:25:55–01:26:20 (busca confusa)
Sem comentário específico capturado nesta janela além de já estar na lista de "brown/warm"
rejeitados citada em MEETING-REQUIREMENTS.md ("rejeitaram bege/marrom (oyster, valley)").

---

## O que isso muda no que já está construído

Conferi cada item concreto e acionável contra o `site/index.html` e `site/styles.css`
atuais do 12-11x-frontier nesta mesma sessão (screenshots reais, não relato do codex):

- Flip cards (fonte: 05-oyster) — IMPLEMENTADO, testado por clique real.
- Tabela comparativa "not under the column" (fonte: 09-hyperbound-ramp) — IMPLEMENTADO,
  confirmado lado a lado por screenshot.
- Preto-e-branco em vez de bege/marrom (fonte da decisão: 10-unify-people, reforçada pela
  rejeição repetida de 05/15/16) — IMPLEMENTADO no hero (people band P&B) e nas seções.
- Marquee de nomes de funcionalidades — IMPLEMENTADO, origem exata não confirmada pelos
  próprios participantes.
- Hero "He's still nodding" como gatilho da escolha do 12 como base — já era a base antes
  mesmo da call, e o hero final trocou de copy mas manteve a mesma lógica de linha de efeito.

**O "signature" da 13-ashby-manifesto — resolvido e implementado.** Fui conferir a própria
página 13 em vez de adivinhar pela fala: `signature-block` lá é uma citação do fundador
("Our branding has really got to be Human plus AI...") assinada como "Russell P." numa fonte
de próprio-punho (Caveat), rotacionada -3deg. Cruzei com PRODUCT.md, que já listava
explicitamente **"a founder statement, one paragraph, signed"** como substituição sancionada
pra seção de depoimento/logo — e com MESSAGE.md, que tem essa MESMA citação, palavra por
palavra, como fala real do fundador na call ("Founder's own words, on the call, when asked
what the brand is"). Ou seja: não é invenção, é a citação já aprovada, no formato que já
tinha sido usado (e aprovado por você) na 13.
Adicionei ao 12-11x-frontier como seção `#founder`, antes do CTA final: kicker "The thesis,
in the founder's own words", blockquote com a citação exata, assinatura "Russell P." em
Caveat na cor ciano da marca, "Founder, PitchGenius.AI" embaixo. Testado com screenshot real
em 1440px e 375px, zero erro de console nos dois.

**04-attio-producttruth nunca foi revisitada nesta call** — não há feedback dela pra aplicar
em lugar nenhum.
