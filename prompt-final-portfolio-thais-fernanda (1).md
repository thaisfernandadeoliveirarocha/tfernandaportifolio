# Prompt final — Portfólio Thais Fernanda

**Versão:** 20/11/2026
**Uso:** cole este prompt numa IA (ou entregue a um desenvolvedor) para recriar, manter ou evoluir o portfólio exatamente como foi aprovado. Se o arquivo `index.html` final estiver disponível, ele é a referência principal; este prompt descreve todas as decisões por trás dele.

---

## 1. Papel e objetivo

Atue como especialista em desenvolvimento front-end, UX/UI e revisão de português do Brasil. Construa (ou mantenha) o portfólio profissional de **Thais Fernanda de Oliveira Rocha**, que atua com educação corporativa, desenvolvimento de pessoas e gestão de projetos e processos, e é criadora do **Método Cultivar**.

O site deve transmitir: **elegância, clareza, credibilidade e acolhimento**. Público principal: recrutadores, gestores de RH/T&D e potenciais clientes.

---

## 2. Regras técnicas de entrega

- **Um único arquivo `index.html`**, com todo o CSS em um bloco `<style>` e todo o JavaScript em `<script>` no próprio arquivo. Nada de arquivos `.css` ou `.js` separados.
- **Todas as imagens embutidas** no HTML como `data:` URI (base64): foto, logo, ícone da aba e ícone do iPhone. Nenhuma pasta `assets/`.
- Único recurso externo: **Google Fonts** (com `preconnect`). Exceção: `og-image.png` e `sitemap.xml` ficam como arquivos ao lado do `index.html` (ver seção 10).
- HTML semântico (`header`, `nav`, `main`, `section`, `article`, `figure`, `blockquote`, `footer`), `lang="pt-BR"`, sem erros no console, sem IDs duplicados, sem links internos quebrados.
- CSS organizado em **um único bloco**, com tokens em `:root` (seção 3) e seções numeradas por comentário. Nunca empilhar vários blocos `<style>` que se sobrescrevem.
- Peso-alvo do arquivo: ~120–135 KB.

---

## 3. Identidade visual (tokens)

### Cores
| Token | Valor | Uso |
|---|---|---|
| `--green` | `#17363A` | cor principal, fundos escuros, títulos |
| `--green-deep` | `#0F2629` | rodapé |
| `--green-soft` | `#244D50` | hover de botões |
| `--sage` | `#688C83` | hover de links |
| `--gold` | `#C9AD79` | destaques sobre fundo escuro |
| `--gold-dark` | `#806124` | destaques sobre fundo claro, números, foco |
| `--ivory` | `#F4F0E8` | fundo claro principal e cabeçalho |
| `--sand` | `#E9EAE2` | fundo claro alternado |
| `--ink` | `#292D30` | texto corrido |
| `--muted` | `#4F665D` | rótulos e itens do menu inativos |
| `--line` | `#17363A24` | linhas finas |
| Verde de status | `#7FD1A8` | ponto “Disponível” e botão “E-mail copiado!” |

### Medidas
- Espaçamentos: 8 / 16 / 24 / 40 / 64 px.
- Padding vertical das seções: `clamp(64px, 9vw, 112px)`; margem lateral: `clamp(18px, 5vw, 32px)`.
- Largura máxima do conteúdo: 1140 px (1260 px a partir de 1600 px; 1400 px a partir de 2200 px).
- **Cantos arredondados:** cards e blocos 16 px; botões 10 px; etiquetas em formato pílula (999 px); foto redonda; ícones em quadrado de 12 px de raio.

### Ritmo de fundos (de cima para baixo)
Hero verde → Sobre marfim → Cases areia → Citação verde (com brilho) → Método marfim → Projetos areia → Contato verde → Rodapé verde mais escuro.

---

## 4. Tipografia

- **Títulos:** `Crimson Pro` (fallback `Crimson Text`, Georgia). Pesos 300, 400, 600 e itálico 400.
- **Textos, menus, botões e rótulos:** `Source Sans 3` (fallback `Source Sans Pro`, Arial). Pesos 400, 600, 700.
- Motivo da escolha: as duas são humanistas e têm alturas de minúsculas parecidas, por isso combinam. (Cormorant Garamond + Manrope foram descartadas por destoarem.)

Regras:
- **Todos os títulos usam serifa** — inclusive os títulos menores dos cards (Estratégia, Clareza, nomes dos projetos, nomes dos canais).
- Nome no hero: Crimson Pro **300** (leve). Títulos de seção: 400. Títulos de cards: 600.
- Texto corrido: 17 px (1.0625rem), entrelinha 1.65. Nenhum texto visível abaixo de 12 px.
- Números sempre com algarismos alinhados (`font-variant-numeric: lining-nums`).
- Rótulos de seção (“01 / QUEM SOU”): 13 px, maiúsculas, espaçamento .18em, cor `--muted`, com **traço dourado de 28 px antes do texto**.
- Títulos de seção: `clamp(2.1rem, 4.2vw, 3.6rem)`, no máximo ~22 caracteres por linha.
- Itálico dourado é o recurso de destaque (slogan, “para pensar / agir / transformar”, “ampliar possibilidades”).

---

## 5. Componentes

- **Botão primário:** fundo verde, texto branco (sobre fundo escuro: fundo dourado, texto verde-escuro). Maiúsculas, 14 px, peso 700, altura mínima 50 px, raio 10 px.
- **Botão secundário:** contorno de 2 px, fundo transparente; no hover, preenche.
- O efeito de “subir” no hover só existe em dispositivos com mouse (`@media (hover:hover)`); no toque, leve redução ao pressionar.
- **Link de texto:** sublinhado fino, peso 700, com seta ↗ quando externo.
- **Bloco de números (“impact”):** fundo verde, raio 16 px, título em serifa, subtítulo com o período, números grandes em dourado com linha dourada acima de cada um. Variações: 3 colunas (padrão), 2 colunas (`.two`), 4 colunas (`.four`, que vira 2×2 no tablet/celular).
- Faixas de destaque dos cards (topo dos cases, lateral do painel) feitas com `box-shadow: inset` para acompanhar os cantos arredondados.

---

## 6. Estrutura e conteúdo, seção por seção

> Use os textos **exatamente** como estão abaixo. Eles já passaram por revisão de português.

### 6.1 Cabeçalho (fixo no topo)
- Fundo **marfim sólido** (sem transparência).
- À esquerda: **logo atual** (versão cursiva “TFernanda” com laço dourado e folhas, sem fundo). Clique leva ao início. `alt="Thais Fernanda"`, `aria-label="Thais Fernanda — voltar ao início"`.
- Alturas do logo: computador **54 px**; tablet e celular **44 px**; celular pequeno (≤380 px) **38 px**; celular deitado **36 px**.
- À direita, menu com 5 itens: **SOBRE · CASES · MÉTODO CULTIVAR · PROJETOS · CONTATO**.
  - Todos com **o mesmo estilo**: maiúsculas, 12,5 px, peso 600, espaçamento .14em, cor `--muted`.
  - **“Contato” NÃO tem caixa/borda** — é igual aos demais.
  - Item da seção atual: cor verde + sublinhado dourado fino logo abaixo da palavra.
- O cabeçalho deve ficar **alinhado com o conteúdo**: logo na mesma linha esquerda dos títulos; último item do menu na mesma linha direita do conteúdo.
- Até 880 px: botão “☰ Menu” (borda 2 px, raio 10 px) que abre lista vertical, com itens separados por traço fino e a seção atual marcada por barra dourada à esquerda. Se não couber na altura da tela, a lista rola por dentro.

### 6.2 Hero (fundo verde)
- Selo em pílula: ponto verde pulsando suavemente + “**Disponível para projetos e oportunidades**”.
- H1: “**Thais Fernanda**”.
- Subtítulo: “Educação corporativa, desenvolvimento de pessoas e gestão de projetos e processos”.
- Traço dourado de 72 px.
- Slogan em itálico dourado: “*Estratégia que organiza. Conhecimento que conecta.*”
- Texto: “Conecto tecnologia, educação corporativa e desenvolvimento humano para transformar conhecimento em experiências de aprendizagem significativas.”
- Botões: **Ver cases** (primário, leva a #cases) e **Vamos conversar** (secundário, leva a #contato).
- **Foto** redonda à direita (até 340 px), com anel dourado fino **concêntrico** (mesma distância em volta toda) e sombra suave. Foto recortada em quadrado com o rosto centralizado e espaço acima da cabeça; resolução 840 × 840.
- Tablet: foto menor ao lado do texto. Celular: foto pequena (~92 px) **ao lado do nome**, para os botões aparecerem na primeira tela.

### 6.3 01 / Quem sou (fundo marfim)
- Título: “Uma trajetória que conecta processos e pessoas.”
- Texto: “Minha experiência profissional reúne projetos tecnológicos, organização de processos, educação corporativa e capacitação de profissionais. Acredito que aprender é ampliar possibilidades — com estratégia, criatividade e respeito às necessidades individuais.”
- Valores em pílulas brancas: Transparência · Autonomia · Respeito · Integridade · Coragem.
- Coluna à direita, alinhada ao título (“Como trabalho”):
  - **Estratégia** — Identificar necessidades, organizar demandas e estruturar caminhos de desenvolvimento.
  - **Aprendizagem** — Transformar conhecimento em experiências relevantes, acessíveis e aplicáveis.
  - **Pessoas** — Reconhecer diferentes trajetórias e estimular autonomia e desenvolvimento contínuo.

### 6.4 02 / Experiências selecionadas (fundo areia)
Título: “Três áreas de atuação. Um propósito.” Três cards (número grande dourado, título em serifa, texto, botão “Explorar case +”):

1. **Educação corporativa** — Organização do conhecimento, de cursos e trilhas educacionais e gestão de ambientes digitais de aprendizagem.
2. **Desenvolvimento de pessoas** — Capacitação técnica e comportamental, orientada às necessidades individuais e às atividades profissionais.
3. **Projetos e processos** — Planejamento, acompanhamento de entregas e análise de processos em contextos de tecnologia e sistemas empresariais.

Todos os painéis seguem a mesma estrutura **Desafio · Atuação · Resultado** + bloco de números.

**Case 01 — Educação corporativa**
- Linha de contexto: “jan. 2024 – nov. 2026 · Aprendizagem digital”
- Desafio: Contribuir para estruturar o conhecimento organizacional de maneira acessível e aplicável.
- Atuação: Organização de conteúdos, estruturação de cursos e trilhas, apoio à administração de plataformas de aprendizagem, comunicação educacional e acompanhamento de indicadores.
- Resultado: Criação de 125 artigos de conhecimento e 147 cursos, integrando tecnologia, conteúdo e experiência de aprendizagem.
- Bloco (2 colunas): “Conhecimento estruturado em números” / “De janeiro de 2024 a novembro de 2026” — **125** artigos de conhecimento · **147** cursos.

**Case 02 — Desenvolvimento de pessoas**
- Linha de contexto: “jan. 2022 – nov. 2026 · Capacitação técnica e comportamental”
- Desafio: Profissionais com experiências distintas precisavam desenvolver conhecimentos técnicos e comportamentais para suas atividades. Minha responsabilidade foi contribuir para essa preparação, respeitando as necessidades individuais.
- Atuação: Capacitação para o exercício das funções e desenvolvimento de competências comportamentais (*soft skills*, marcado com `lang="en"`), conforme as necessidades individuais observadas, com orientação contextualizada ao trabalho.
- Resultado: Acompanhamento da trajetória dos 50 profissionais capacitados no período, com evolução profissional relatada na grande maioria dos casos.
- Bloco (3 colunas): “Trajetória dos profissionais acompanhados” / “De janeiro de 2022 a novembro de 2026” — **50** profissionais capacitados · **40** promoções internas · **5** oportunidades em outras empresas. Abaixo: “**47 de 50 (94%)** com evolução profissional relatada, incluindo 2 pessoas com outras evoluções nas atividades.”
- Nota recolhível (`<details>`) “Como esses dados foram levantados”: Dados de acompanhamento relatados pela profissional, com divulgação agregada autorizada pela empresa. Referência desta versão: 04/11/2026. Não houve auditoria independente, grupo de comparação nem avaliação padronizada antes e depois das capacitações; por isso, os números descrevem trajetórias e não comprovam relação de causa e efeito. O fato de 3 participantes não terem desfecho classificado não indica ausência de aprendizagem. Nenhum dado pessoal é apresentado. Esses indicadores são anteriores ao Método Cultivar e não correspondem a resultados de sua aplicação.
- Todas as ressalvas ficam **apenas** nessa nota — nada de avisos espalhados pela página.

**Case 03 — Gestão de projetos e processos**
- Linha de contexto: “Tecnologia · Sistemas empresariais”
- Desafio: Apoiar a execução de projetos ERP, conciliando requisitos técnicos, prazos, comunicação e necessidades dos clientes.
- Atuação: Planejamento e acompanhamento de projetos, análise de processos, resolução de problemas e articulação entre equipes.
- Resultado: Participação em mais de 200 projetos ERP e histórico de 650 implantações, com prazo médio de 69,5 dias diante de uma meta de 72 dias e avaliação máxima de satisfação do cliente (CSAT 5/5). (“CSAT 5/5” com espaço não separável.)
- Bloco (4 colunas): “Projetos e implantações em números” / “Histórico de atuação em projetos ERP” — **200+** projetos ERP · **650** implantações · **2,5 dias** abaixo da meta, em média · **5/5** CSAT (satisfação do cliente).

### 6.5 Citação “Minha convicção” (fundo verde com brilho radial)
- Duas linhas douradas finas, esmaecidas nas pontas, no topo e na base da faixa.
- Aspas “ grandes em dourado → rótulo “MINHA CONVICÇÃO” entre dois traços dourados → frase em serifa leve (300), duas linhas equilibradas, máx. ~17 caracteres por linha: “Desenvolver pessoas é *ampliar possibilidades.*” (trecho final em itálico dourado, sem quebrar no meio).
- Traço dourado de 40 px → assinatura em itálico “*Thais Fernanda*” → linha “CRIADORA DO MÉTODO CULTIVAR” (maiúsculas pequenas, cinza-esverdeado).
- Marcação: `figure` + `blockquote` + `figcaption` + `cite`.

### 6.6 03 / Método autoral (fundo marfim)
- Título: “Método Cultivar. Compreender. Aplicar. Evoluir.”
- Texto: “Uma metodologia de desenvolvimento humano aplicado, organizada em três movimentos contínuos. Atualmente, está em fase de estruturação e validação.”
- Três etapas em cards brancos, com **números grandes em serifa dourada (01, 02, 03)** seguidos de linha dourada que esmaece — **sem bolinhas/círculos**. Setas → entre as etapas (↓ no celular):
  - **01 Clareza** — *para pensar* — Escutar e diagnosticar necessidades, competências e prioridades.
  - **02 Coerência** — *para agir* — Planejar e experimentar comportamentos e ações em situações reais.
  - **03 Compromisso** — *para transformar* — Acompanhar evidências, aprender e evoluir com responsabilidade.
- Ícone de ciclo + “O ciclo recomeça a cada nova etapa de desenvolvimento.”
- “FERRAMENTAS EM DESENVOLVIMENTO” em pílulas: Mapa de Clareza · Plano de Coerência · Diário de Aplicação · Painel de Compromisso.
- Botão primário: “Conversar sobre o método” → `mailto:tfernanda@live.com?subject=Interesse%20no%20M%C3%A9todo%20Cultivar`.

### 6.7 04 / Projetos e iniciativas (fundo areia)
- Título: “Ideias que ganham forma.” Texto: “Experiências em aprendizagem digital, conteúdo e desenvolvimento profissional.”
- Três cards com ícone de traço fino centralizado em quadrado arredondado branco:
  - **Newsletter Gente que Pensa** — Reflexões e conteúdos sobre desenvolvimento humano, aprendizagem e futuro do trabalho. Link “Ler newsletter ↗”.
  - **Ambientes digitais de aprendizagem** — Organização de cursos, trilhas e conteúdos, com experiência em gestão e melhoria contínua de plataformas LMS. (ícone de camadas com 3 níveis, centralizado)
  - **Comunicação educacional** — Vivência em iniciativas de catálogo de cursos, formatos de podcast corporativo e projetos de aprendizagem digital.

### 6.8 05 / Conexões (fundo verde) — contato e canais unificados
- Título: “Vamos conversar sobre novas possibilidades?”
- Texto: “Estou aberta a conexões e conversas profissionais sobre aprendizagem corporativa, desenvolvimento humano e gestão de projetos e processos.”
- Botões: **Enviar e-mail** (`mailto:tfernanda@live.com?subject=Contato%20profissional`, manter assim) e **Copiar e-mail** (copia o endereço, fica verde e mostra “E-mail copiado!” por 2,5 s, com aviso para leitor de tela e alternativa caso a área de transferência falhe).
- Seis cards de canais (ícone dourado centralizado em quadrado arredondado, título em serifa, descrição, seta ↗):

| Canal | Descrição | Link |
|---|---|---|
| LinkedIn profissional | Trajetória e conexões | https://www.linkedin.com/in/tfernanda/ |
| Currículo digital | Experiência e competências | https://thaisfernandadeoliveirarocha.github.io/thaisfernandacvdigital/ |
| Newsletter Gente que Pensa | Artigos e reflexões | https://www.linkedin.com/newsletters/gente-que-pensa-7243262984125399040 |
| Portfólio Behance | Projetos e criação visual | https://www.behance.net/tfernanda |
| Instagram | @tfernanda_oficial | https://www.instagram.com/tfernanda_oficial/ |
| Comunidade no WhatsApp | Troca e pertencimento | https://chat.whatsapp.com/Buo2TJmos7qBcIYA2nlKcb |

- Todos os links externos: `target="_blank" rel="noopener noreferrer"` + texto oculto “(abre em nova aba)” para leitores de tela.

### 6.9 Rodapé (verde mais escuro)
- À esquerda: “© 2026 THAIS FERNANDA · ESTRATÉGIA / APRENDIZAGEM / PESSOAS”.
- À direita: “Atualizado em novembro de 2026” (com `<time>`).
- **Sem links** de LinkedIn, Instagram ou e-mail no rodapé. Texto (não logo).
- No celular: as duas linhas empilhadas e alinhadas à esquerda.

---

## 7. Comportamentos (JavaScript)

1. **Menu ativo:** marca a seção que **ocupa mais espaço visível** na tela (descontando o cabeçalho). Enquanto o hero domina a tela, nenhum item fica marcado. No fim da página, marca “Contato”. Usar `aria-current="location"`. Atualização com `requestAnimationFrame`.
2. **Cases:** só um painel aberto por vez; botão alterna entre “Explorar case +” e “Fechar case −” com `aria-expanded`; card ativo ganha faixa dourada. No computador o painel abre **abaixo da grade**; no tablet/celular (≤880 px) abre **logo abaixo do card tocado**. Rolagem suave só até o necessário (`block: 'nearest'`).
3. **Menu do celular:** abre/fecha pelo botão; fecha ao clicar num item, ao clicar fora e ao voltar para tela larga. **Esc só age quando o menu está aberto** (fecha e devolve o foco ao botão).
4. **Entrada suave** de títulos, cards, etapas e canais ao rolar (opacidade + deslocamento de 24 px), com pequeno atraso escalonado. Conteúdo visível mesmo sem JavaScript (classe `js` no `<html>`).
5. **Voltar ao topo:** botão redondo verde com seta dourada e contorno dourado sutil, aparece após rolar 1,2 tela; **sobe junto quando o rodapé aparece**, para não cobrir nada.
6. **Copiar e-mail:** ver seção 6.8.
7. **Impressão:** antes de imprimir, abre a nota “Como esses dados foram levantados”.
8. Respeitar `prefers-reduced-motion`: sem animações, sem pulso no selo, rolagem instantânea.

---

## 8. Responsividade

Testar e garantir, **sem rolagem lateral** e com áreas de toque ≥ 44 px, em: 320 × 568, 360 × 780, 390 × 844, 430 × 932, 844 × 390 (deitado), 768 × 1024, 820 × 1180, 1024 × 1366, 1180 × 820, 1280 × 720, 1440 × 900, 1920 × 1080 e 2560 × 1440.

- Pontos de quebra: 1020 px (grades de 3 → 2 colunas), 880 px (menu vira botão; cases e projetos em 1 coluna), 600 px (hero com foto ao lado do nome; botões em largura total), 380 px (ajustes finos).
- Celular deitado (altura ≤ 520 px): cabeçalho de 60 px, hero compacto, foto ao lado.
- Celular pequeno em pé (≤ 600 × 700): hero compacto para o botão principal aparecer na primeira tela.
- Telas grandes: fonte-base 106,25% (≥1600 px) e 118,75% (≥2200 px).
- `viewport-fit=cover` e respeito às áreas seguras do iPhone (cabeçalho, rodapé e botão “voltar ao topo”).

---

## 9. Acessibilidade

- Link invisível “**Pular para o conteúdo**” como primeiro item do Tab, levando a `<main id="conteudo">`.
- Contraste mínimo WCAG AA em todos os textos (foco: contorno dourado-escuro sobre fundo claro; dourado claro sobre fundo escuro).
- Ordem correta de títulos (um único H1).
- Todas as imagens com `alt`; ícones decorativos com `aria-hidden`.
- Painéis dos cases com `role="region"` e `aria-labelledby`.

---

## 10. Metadados e SEO

- `<title>`: “Thais Fernanda | Educação corporativa e desenvolvimento de pessoas” (maiúscula só no início, como manda o português).
- `description`: “Portfólio de Thais Fernanda: educação corporativa, desenvolvimento de pessoas e gestão de projetos e processos. Conheça os cases, o Método Cultivar e os canais de contato.”
- Endereço publicado: **https://thaisfernandadeoliveirarocha.github.io/tfernandaportifolio/** (GitHub Pages).
- `<link rel="canonical">` e `og:url` com esse endereço.
- Open Graph completo (`og:type`, `og:locale` pt_BR, `og:site_name`, `og:title`, `og:description`) e `twitter:card="summary_large_image"`.
- **Imagem de compartilhamento:** `og-image.png` (1200 × 630, fundo marfim, moldura dourada fina, logo centralizado e a linha “EDUCAÇÃO CORPORATIVA · DESENVOLVIMENTO DE PESSOAS · PROJETOS E PROCESSOS”), publicada **na mesma pasta do `index.html`** e referenciada por URL absoluta em `og:image` e `twitter:image`, com largura, altura e texto alternativo. É o único arquivo de imagem fora do HTML, porque as redes exigem endereço público.
- `sitemap.xml` na mesma pasta, com o endereço do site.
- JSON-LD `Person`: `url` do site, `image` (og-image.png), nome completo, `alternateName` “Thais Fernanda”, `jobTitle` “Educação corporativa e desenvolvimento de pessoas”, `description` mencionando “Criadora do Método Cultivar”, e-mail, endereço (Várzea Paulista – SP, BR), áreas de conhecimento e `sameAs` (LinkedIn, Behance, Instagram, currículo digital).
- `theme-color` `#17363A`.

---

## 11. Imagens e marca

- **Logo do cabeçalho:** versão cursiva “TFernanda” com laço dourado e folhas. Fundo creme removido com bordas suaves (sem perder as cores sólidas) e pontinhos soltos limpos. Embutido em WebP com transparência, em resolução 2× da altura exibida (~27 KB).
- **Ícone da aba (64 px) e do iPhone (180 px):** monograma “TF” cursivo do logo atual, com o laço dourado, sobre quadrado marfim de cantos arredondados; pontas da direita esmaecidas suavemente; legível a 16 px.
- **Foto:** retrato profissional, recorte quadrado com o rosto centralizado, WebP 840 × 840 (≈ 23 KB), exibida em círculo.
- Peso das imagens embutidas: logo ≈ 27 KB, foto ≈ 23 KB, ícones ≈ 1–4 KB.

---

## 12. Impressão / PDF

Fundo branco; sem cabeçalho, botões, selo nem animações; os três cases abertos; nota metodológica expandida; endereço dos links externos visível entre parênteses; cards sem quebra no meio.

---

## 13. Revisão de português aplicada (manter)

- Meses em minúsculas e abreviados com ponto (“jan. 2024 – nov. 2026”).
- Termos estrangeiros consolidados mantidos (*cases*, *newsletter*, *podcast*, LMS, ERP, CSAT); *soft skills* acompanhado de “competências comportamentais”.
- Títulos em português sem maiúscula em cada palavra.
- “Esses” para retomar algo já dito; vírgulas em torno de “por isso”; paralelismo de artigos nas enumerações.
- “2,5 dias abaixo da meta, em média” (e não “abaixo da meta média”).

---

## 14. O que NÃO fazer

- Não separar o código em vários arquivos nem criar pasta de imagens.
- Não colocar caixa/borda no “Contato” do menu.
- Não colocar links de LinkedIn, Instagram ou e-mail no rodapé, nem trocar o texto do rodapé por logo.
- Não usar encurtadores de link (ex.: goo.su).
- Não espalhar ressalvas pela página — só na nota recolhível do case 02.
- Não usar bolinhas com números nas etapas do Método.
- Não deixar o anel da foto deslocado; ele é concêntrico.
- Não trocar o botão “Enviar e-mail” por formulário (decisão atual).
- Não reintroduzir o par de fontes Cormorant Garamond + Manrope.
- Não inventar dados, ferramentas, empresas ou depoimentos.

---

## 15. Pendências (dependem da Thais)

1. ~~Ativar imagem de compartilhamento, `og:url` e `canonical`~~ — feito em 20/11/2026. Opcional: cadastrar o site no Google Search Console e enviar o `sitemap.xml`.
2. **Conferir no site publicado:** clicar em cada link externo (atenção ao convite do WhatsApp, que pode expirar) e confirmar se o selo “Disponível para projetos e oportunidades” continua válido.
3. **Opcional:** ferramentas usadas e prints anonimizados dos cases (há modelos comentados no código); depoimentos com autorização; currículo em PDF; período do case 03.
4. **Manutenção:** atualizar “Atualizado em …” no rodapé a cada nova versão.

---

## 16. Checklist de verificação antes de entregar qualquer alteração

- [ ] Sem rolagem lateral nos 13 tamanhos de tela da seção 8.
- [ ] Botões e links com área de toque ≥ 44 px; nenhum texto < 12 px.
- [ ] Menu marca a seção certa ao rolar (nenhum no hero, “Contato” no fim).
- [ ] Cases abrem no lugar certo (abaixo da grade no computador, abaixo do card no celular).
- [ ] Esc, “Pular para o conteúdo” e foco visível funcionando pelo teclado.
- [ ] Contraste AA, IDs únicos, âncoras válidas, `alt` em todas as imagens, console sem erros.
- [ ] Teste no PageSpeed Insights e em um iPhone real (Safari) após publicar.
- [ ] Sempre partir da **versão mais recente** do `index.html`, para não perder ajustes.
