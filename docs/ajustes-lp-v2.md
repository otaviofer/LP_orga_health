# Ajustes da LP v2 — OrgaHealth

Status: **executado no HTML** (17/11/2026) — `orga-health-lp-v2.html`, testado em 390, 820 e 1440 px sem rolagem horizontal.
Figma: página **"LP v2 — ajustes 17/11"** criada no arquivo OrgaHealth (Desktop 1440 + Mobile 390). Pendências no Figma (bloqueado pelo limite de chamadas do plano Starter):
- Mobile: os botões dourados ficaram sem o círculo da seta visível (ajustar a largura do texto do botão, ~250 px).
- Conferir a logo da V4 no rodapé (imagem branca enviada; verificar se aparece).
- Botão "Fale com um especialista": trocar a seta pelo ícone do WhatsApp.

- Logo horizontal: o recorte do SVG cortava a ponta do coração (corrigido no HTML; no Figma ajustar o componente "Logo/Horizontal branca (oficial)").
- Hero sem o coração de fundo e com degradê vermelho escuro; "100% carteira médica" numa fonte só; FAQ centralizado (aplicar também no Figma).

## Parte 9 — Ajustes finais (18/11/2026) — executado no HTML
20. Hero: retirado o coração de fundo; fundo com **degradê vermelho escuro** (#591114 → #2A0608), a pedido do Otávio (exceção à regra "sem degradês" do manual).
21. "**100% carteira médica**" numa única fonte e cor (Manrope ExtraBold, marsala), tamanho reduzido.
22. FAQ **centralizado** na página. Revisão (18/11): a conversa virou uma coluna centralizada (620 px) com as perguntas alinhadas à esquerda dentro dela, e a **resposta abre logo abaixo, alinhada à borda esquerda da pergunta**, sobrepondo levemente o balão (como na referência), com o avatar da Orga do lado de fora.
23. Logo horizontal: recorte do SVG corrigido para não cortar a ponta do coração (em todos os lugares: topo, header fixo e rodapé).

Assets: `assets-lp/equipe-medica.png` (gerada por IA e recortada) · `assets-lp/logo-v4-borges-branca.webp`.
Paleta aplicada: a oficial do conta-gotas (skill identidade-orga) — Marsala #591114, Dourado #BA8539, Creme #F8F3ED, Grafite #262626.

## Decisões finais (17/11/2026)
- **100%, e não 90%**: trocar todas as ocorrências de "90%" por "100%" (número grande "100%" + "carteira médica" em uma linha; textos da seção 2, do pilar "Foco exclusivo em saúde" e da objeção 1).
- **Foto da equipe**: pode buscar na internet, Magnific ou Designi.
- **CTAs novos**: criar a frase de acordo com cada seção.
- **Moldura do card do formulário**: sai também.
- **Endereço no rodapé**: o Otávio confirma e coloca depois (manter como está).
Arquivo alvo: `orga-health-lp-v2.html`

## Parte 1 — Cores e hero (17/11/2026)

1. A cor predominante da hero section deve ser o **vermelho (marsala #7A1F28)** da paleta, no lugar do azul-marinho.
2. Retirar a **curva/onda** de transição entre o hero e a seção seguinte (marsala + fio dourado + botão de seta redondo).
3. Retirar os **cards pequenos sobre o vídeo** ("90% da carteira são médicos" e "Suporte 24h com validação humana").
4. Usar as **logos oficiais em SVG** da pasta do cliente no lugar do símbolo redesenhado:
   `4.0 Documentos Gerais/4.3 Design/4.3.1 Identidade Visual/SVG/`
   - BRANCA: Logo_banca_hor, Logo_branca_vert, Isotipo_branca, Logotipo_branca
   - VERMELHA: Logo_principal_hor/vert, Isotipo_principal, Logotipo_principal
   - AZUL: Logo_azul_hor/vert, Isotipo_azul, Logotipo_azul
   - MONOCROMÁTICA: versões B e P (hor, vert, isotipo, logotipo)

## Parte 2 — Seção "Contabilidade 100% focada" e header (17/11/2026)

5. No lugar do quadro de foto: **foto de uma equipe médica (2 ou 3 pessoas) em PNG recortado**, com **animação ao aparecer**, e a base da foto **desaparecendo num degradê** para o fundo (sem corte seco).
6. **Header fixo (dock)** na cor **vermelho marsala** da paleta, com a **logo horizontal branca** (`SVG/BRANCA/Logo_banca_hor.svg`).
7. Retirar o **identificador de seção** ("01 —", "02 —", "03 —"...) de **todas** as seções.
8. Fundo desta seção na **mesma cor das seções abaixo** (hoje creme #F7F3EF; passa a ser o mesmo tom das demais).
9. Número grande: **"100%"** no lugar de "90%", com a legenda **"carteira médica" em uma linha só**.
   - ⚠ Pendente de confirmação: conflito com "carteira 90% médica" do briefing/texto da mesma seção (sugestão: legenda "100% focada em médicos e clínicas").
   - ⚠ Pendente de confirmação: origem da foto da equipe (foto real da pasta do cliente / imagem gerada por IA / espaço pronto para o PNG).

## Parte 3 — Seção Diferenciais "Especialização médica que protege seu patrimônio" (17/11/2026)

10. Deixar a seção **mais personalizada no estilo da referência** (grade de FAQ "Your questions resolved in one place" — só o estilo, não o conteúdo):
    - Os 4 pilares ficam **soltos, sem o painel/moldura** em volta, cada um com ícone em círculo/contorno no topo, título e texto abaixo.
    - **Hover:** ao passar o mouse, uma **box vermelha (marsala)** aparece atrás do item com **fade**, o **texto fica branco** (ícone também invertido) e a **box cresce um pouco** (scale leve).
    - Manter acessível: mesmo efeito no foco por teclado; no celular (sem hover), avaliar estado ativo ao tocar ou o primeiro item já destacado, como na referência.

## Parte 4 — Seção Dúvidas frequentes (17/11/2026)

11. FAQ no **estilo conversa** da referência (só o estilo):
    - Cada pergunta vira um **balão de mensagem** (escuro) com um botão **"+"** ao lado.
    - Ao clicar no "+", a **resposta aparece como um balão de resposta** (claro, com sombra), como uma conversa, com um **avatar da Orga Health** (isotipo) ao lado do balão de resposta. O "+" vira "−" para fechar.
    - Bloco centralizado, título "Dúvidas frequentes" no topo; manter as 4 objeções com o texto exato do briefing.
    - Acessível: botão com `aria-expanded`, funciona no teclado; animação curta de entrada do balão (fade + leve subida), respeitando "reduzir movimento".

## Parte 5 — CTA em todas as seções (17/11/2026)

12. Colocar **botão de CTA em cada seção que ainda não tem**, com a frase de acordo com o assunto da seção. Hoje têm CTA: Hero, Contabilidade 100% focada, Formulário, Presença física. Faltam: **Diferenciais, Depoimentos e Dúvidas frequentes**.
    - Frases sugeridas (aguardando aprovação):
      - Diferenciais → "Quero uma contabilidade feita para médicos"
      - Depoimentos → "Quero ser atendido pela Orga Health"
      - Dúvidas frequentes → "Fale com um especialista" (frase do próprio briefing; pode abrir o WhatsApp)

## Parte 6 — Seção Formulário (17/11/2026)

13. Seção aprovada. **Manter o fundo azul-marinho**, mas **retirar os degradês** (o brilho marsala no canto superior direito e o brilho dourado no canto inferior esquerdo): fundo azul chapado.
    - ⚠ Pendente de confirmação: o recorte enviado mostra a moldura dupla (borda externa fina) do card do formulário — confirmar se é para retirá-la também ou só o degradê.

## Parte 7 — Seção Presença física (17/11/2026)

14. Seção aprovada. **A foto da sede será providenciada pelo Otávio** (manter o espaço pronto).
15. O **card do mapa** passa a ser **clicável** e abre o **Google Maps em nova aba**, usando o mesmo mapa/endereço do site do cliente (orgahealth.com.br):
    - Endereço (do site): **Rua Mariano de Campos Maia (Alameda), Ponte Nova – Construmat, Várzea Grande – MT, 78115-245**
    - Link do mapa usado no site: `https://maps.google.com/maps?q=Rua Mariano de Campos Maia (Alameda), Ponte Nova - Construmat, Várzea Grande - MT, 78115-245`
    - Aplicar: o card do mapa mostra o **mapa do Google embutido** (igual ao do site) e todo o card vira link para abrir no Google Maps (nova aba, `rel="noopener"`).
    - Sugestão extra: usar esse endereço no rodapé, no lugar de "[endereço completo a confirmar]".

## Parte 8 — Rodapé e botões flutuantes (17/11/2026)

16. Rodapé aprovado; **usar apenas o fundo vermelho (marsala)**, sem o degradê para o azul.
17. Adicionar um **campo pequeno no rodapé** indicando que a LP foi **desenvolvida pela V4 Borges & Co**, com a **logo da V4** (arquivo enviado, salvo em `assets-lp/logo-v4-borges-branca.webp`, versão branca).
18. Botão do **WhatsApp com efeito pulsando o tempo todo** para chamar atenção (anel pulsando em volta; respeitar "reduzir movimento").
19. **Botão "voltar ao topo"** à esquerda do WhatsApp, com seta para cima; ao clicar, rola suavemente até o topo da página.
