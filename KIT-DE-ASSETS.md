# Kit de assets · como montar para qualquer marca

Guia para o time montar a pasta de arquivos de uma marca nova e subir no manual, sem precisar mexer em código.

**A regra de ouro:** o manual procura cada imagem por um **nome fixo**. Se o arquivo tiver o nome e a pasta certos, ele aparece no lugar certo. Se faltar, aparece um placeholder cinza e nada quebra.

---

## Regras gerais

- **Nomes:** tudo em minúsculas, sem acento, sem espaço e sem cedilha. Use hífen: `horizontal-positivo.svg`, não `Horizontal Positivo.svg`.
- **Extensão:** use exatamente a da lista (`.svg`, `.jpg`, `.png`). Um `.png` no lugar de um `.svg` não aparece.
- **Números com dois dígitos:** `foto-01.jpg`, não `foto-1.jpg`.
- **SVG:** contornos convertidos (sem texto vivo), sem fundo e com margem mínima. Exporte pelo Illustrator com "Export As → SVG".
- **Fotos (JPG):** até 2.000 px no lado maior e até 500 KB. Use "Export for Web" com qualidade de 70 a 80%.
- **PNG (exemplos de peças):** até 2.000 px e até 1 MB.
- **Peso total:** até 3 MB por arquivo. Vídeos e arquivos abertos (AI, PSD, INDD) não vão no manual; use um link do Drive.
- **Deixe de fora o que não existe.** Se a marca não tem assinatura com tagline, por exemplo, não crie o arquivo e avise quem edita o `brand.js` para remover essa versão.

---

## Estrutura da pasta

Monte uma pasta `assets` no computador com exatamente estas subpastas:

```
assets/
  logos/
    assinaturas/
      pacotes/
  fonts/
  fotos/
    aplicacao/
    arquitetura/
    dress-code/
    produto/
  diagramas/
    alinhamento/
    figura-fundo/
    grafismos/
    grid/
      formatos/
    reducao/
  events/
  submarcas/        (só se a marca tiver sub-marcas)
```

---

## 1. Logos · `assets/logos/`

| Arquivo | O que é | Onde aparece |
|---|---|---|
| `logo-principal.svg` | assinatura principal, colorida | menu lateral, capa |
| `logo-simplificada.svg` | versão reduzida | capa e Assinaturas |
| `logo-negativo.svg` | principal em branco | fundos escuros |
| `simbolo.svg` | só o símbolo | ícone da aba do navegador |

### Assinaturas · `assets/logos/assinaturas/`

Cada versão da assinatura tem **3 arquivos**: colorida, positivo (100% preto) e negativo (100% branco).

| Versão | Arquivos |
|---|---|
| Horizontal | `horizontal-colorida.svg` · `horizontal-positivo.svg` · `horizontal-negativo.svg` |
| Horizontal com tagline | `horizontal-tagline-colorida.svg` · `horizontal-tagline-positivo.svg` · `horizontal-tagline-negativo.svg` |
| Vertical | `vertical-colorida.svg` · `vertical-positivo.svg` · `vertical-negativo.svg` |
| Vertical com tagline | `vertical-tagline-colorida.svg` · `vertical-tagline-positivo.svg` · `vertical-tagline-negativo.svg` |
| Símbolo | `simbolo-colorida.svg` · `simbolo-positivo.svg` · `simbolo-negativo.svg` |

### Pacotes de download · `assets/logos/assinaturas/pacotes/`

Um `.zip` por versão e formato, com todas as cores dentro. Esses arquivos alimentam os botões de download.

```
horizontal-svg.zip           horizontal-png.zip           horizontal-pdf.zip
horizontal-tagline-svg.zip   horizontal-tagline-png.zip   horizontal-tagline-pdf.zip
vertical-svg.zip             vertical-png.zip             vertical-pdf.zip
vertical-tagline-svg.zip     vertical-tagline-png.zip     vertical-tagline-pdf.zip
simbolo-svg.zip              simbolo-png.zip              simbolo-pdf.zip
```

O botão "Baixar todas as versões" monta o pacote completo sozinho, então não precisa de arquivo para ele.

---

## 2. Fontes · `assets/fonts/`

| Arquivo | O que é |
|---|---|
| `fonte-display.zip` | família de títulos, para download |
| `fonte-display-licenca.txt` | licença ou link da fundição |
| `fonte-texto.zip` | família de texto corrido, para download |
| `fonte-texto-licenca.txt` | licença ou link |
| `fonte-sub-marca.zip` + `fonte-sub-marca-licenca.txt` | só se a marca tiver sub-marcas |

Para o manual **exibir** os textos na fonte da marca, inclua também os arquivos web de cada peso, em `.woff2` (preferível) ou `.otf`. Siga este padrão de nome:

```
display-800.woff2      texto-400.woff2      texto-700.woff2
```

Esses arquivos precisam ser registrados no `brand.js` (veja "Dados da marca", no fim deste guia). Se a fonte for do Google Fonts, não precisa de arquivo: basta o link.

Atenção à licença: só publique o `.zip` da fonte se a licença permitir distribuição. Se não permitir, deixe só o `-licenca.txt` com o link da fundição.

---

## 3. Fotos · `assets/fotos/`

| Arquivo | Onde aparece |
|---|---|
| `conceito-destaque.jpg` | Expressão visual → Conceito (logo aplicado, imagem grande) |
| `persona.jpg` | Personalidade → Brand persona |
| `foto-01.jpg` a `foto-06.jpg` | galerias de imagem do Posicionamento |
| `tratamento-01.jpg`, `tratamento-02.jpg` | Expressão visual → Imagens (tratamento fotográfico) |
| `slogan-fundo.jpg` | opcional: fundo do quadro do slogan |
| `aplicacao/aplicacao-foto-01.jpg`, `-02.jpg` | Aplicação da marca → Sobre fotos (foto clara e foto escura) |
| `arquitetura/arquitetura-01.jpg` a `-03.jpg` | Experiência → Arquitetura e ambientes |
| `produto/produto-01.jpg` a `-03.jpg` | Experiência → Características |
| `dress-code/dress-code-01.jpg` a `-03.jpg` | Cultura → Dress code |

Formato horizontal (3:2 ou 16:9) para todas, menos `persona.jpg`, que funciona melhor vertical ou quadrada.

---

## 4. Diagramas · `assets/diagramas/`

São as imagens técnicas montadas no Illustrator a partir do logo da marca. Use SVG em todos.

### Grid e arejamento · `diagramas/grid/`
Para cada versão da assinatura, **2 arquivos**:
```
horizontal-grid.svg           horizontal-arejamento.svg
horizontal-tagline-grid.svg   horizontal-tagline-arejamento.svg
vertical-grid.svg             vertical-arejamento.svg
vertical-tagline-grid.svg     vertical-tagline-arejamento.svg
simbolo-grid.svg              simbolo-arejamento.svg
```

### Redução · `diagramas/reducao/`
Um por versão: `horizontal-reducao.svg`, `horizontal-tagline-reducao.svg`, `vertical-reducao.svg`, `vertical-tagline-reducao.svg`, `simbolo-reducao.svg`.

### Alinhamento · `diagramas/alinhamento/`
Para cada versão, **4 exemplos**: preferencial, secundário e dois indevidos.
```
horizontal-preferencial.svg   horizontal-secundario.svg
horizontal-indevido-1.svg     horizontal-indevido-2.svg
```
Repita o padrão para `horizontal-tagline-`, `vertical-`, `vertical-tagline-` e `simbolo-`.

### Usos indevidos · direto em `diagramas/`
Dois exemplos (a e b) por erro:
```
uso-incorreto-01a.svg   uso-incorreto-01b.svg
uso-incorreto-02a.svg   uso-incorreto-02b.svg
uso-incorreto-03a.svg   uso-incorreto-03b.svg
```
Para ter mais erros, continue a numeração (`04a`, `04b`…) e avise quem edita os textos para incluir o título de cada um.

### Figura e fundo · `diagramas/figura-fundo/`
`correto-01.svg` a `correto-03.svg` e `indevido-01.svg` a `indevido-03.svg`.

### Elementos gráficos · `diagramas/grafismos/`
| Arquivo | O que é |
|---|---|
| `grafismo-01.svg` a `-03.svg` | cada família de grafismo isolada |
| `composicao-01.svg` a `-03.svg` | exemplos de uso em composição |
| `correto-01.svg` a `-03.svg` | usos corretos |
| `indevido-01.svg` a `-06.svg` | usos indevidos |

### Grid de layout
| Arquivo | Onde aparece |
|---|---|
| `diagramas/grid-modular.svg` | Layouts → Grid (estrutura base) |
| `diagramas/grid/formatos/grid-quadrado.svg` | adaptação para formato quadrado |
| `diagramas/grid/formatos/grid-vertical.svg` | formato vertical (post 4:5) |
| `diagramas/grid/formatos/grid-stories.svg` | formato stories (9:16) |
| `diagramas/grid/formatos/grid-horizontal.svg` | formato horizontal (16:9) |
| `diagramas/grid/formatos/grid-a4.svg` | impresso A4 |
| `diagramas/layout-01.svg` a `-04.svg` | Layouts → Composição (proporção da marca com outros elementos) |

---

## 5. Exemplos de layouts · `assets/events/`

As peças aplicadas que aparecem no carrossel de Exemplos.
```
exemplo-01.png   exemplo-02.png   …   exemplo-08.png
```
O manual mostra quantos arquivos existirem nessa sequência, até o número definido no conteúdo (8 no template). Para ter mais, continue a numeração e avise quem edita o conteúdo. Pode ser JPG em vez de PNG, desde que o conteúdo também seja ajustado. O mais simples é manter PNG.

---

## 6. Sub-marcas · `assets/submarcas/` (só se existirem)

Use o nome da sub-marca sem acento como prefixo (ex.: `produto-a`):

| Arquivo | O que é |
|---|---|
| `<nome>-principal.svg` · `<nome>-principal-negativa.svg` | assinatura principal |
| `<nome>-simplificada.svg` · `<nome>-simplificada-negativa.svg` | assinatura simplificada |
| `<nome>-aplicacao-01.png` · `<nome>-aplicacao-02.png` | exemplos aplicados |
| `nivel-2-grid.svg` | grid de construção das assinaturas do nível 2 |

Como os nomes das sub-marcas mudam a cada marca, eles também precisam ser cadastrados no conteúdo.

---

## Como subir no manual

1. Monte a pasta `assets` completa no computador, seguindo este guia.
2. No GitHub, abra o repositório da marca (ex.: `MotoraDesign/manual-nome-da-marca`).
3. Abra o endereço de upload, que já aponta para a pasta certa:
   `https://github.com/MotoraDesign/<repositorio>/upload/main/assets`
4. Confira se o topo da página mostra `<repositorio> / assets /`.
5. Arraste as **subpastas** (`logos`, `fotos`, `diagramas`…), não a pasta `assets` inteira.
6. Arquivos com o mesmo nome **substituem** os placeholders automaticamente.
7. Clique em **Commit changes**. O site atualiza em cerca de 1 minuto.

**Limite de 100 arquivos por envio.** Se passar disso, suba em rodadas: primeiro `logos` e `fonts`, depois `fotos`, depois `diagramas`, e por fim `events` e `submarcas`.

**Imagens pontuais** (trocar uma foto, por exemplo) podem ser trocadas direto pelo painel, no modo edição, sem passar pelo GitHub.

---

## Dados da marca (`content/brand.js`)

Os arquivos sozinhos não mudam **cores, nomes de fonte nem a lista de assinaturas**. Esses dados ficam no `content/brand.js` e são preenchidos pelo **Painel de manuais → Dados da marca**, no card do manual: um formulário que grava o arquivo sozinho, sem mexer em código.

No formulário, trocar o HEX de uma cor atualiza essa cor em todo o manual. RGB e CMYK são calculados sozinhos; corrija com os valores oficiais, se houver.

Use esta ficha para reunir os dados antes:

```
NOME DA MARCA (grafia oficial):
TAGLINE:
SLOGAN:

CORES PRINCIPAIS (nome · HEX · RGB · CMYK · Pantone):
1.
2.
3.
CORES DE APOIO:
NEUTRAS (incluir preto e branco):

FONTE DE TÍTULOS (nome · pesos usados · link da fundição):
FONTE DE TEXTO (nome · pesos usados · link da fundição):
FONTE DE SUB-MARCAS (se houver):

ASSINATURAS QUE EXISTEM (marque):
[ ] horizontal  [ ] horizontal com tagline  [ ] vertical  [ ] vertical com tagline  [ ] símbolo
TAMANHO MÍNIMO de cada uma (impresso em mm · digital em px):

TEM SUB-MARCAS? (sim/não) Se sim, nomes e nível de cada uma:
```

Textos de posicionamento, cultura, personalidade etc. **não** precisam de ficha: são preenchidos direto no modo edição pelo painel.

---

## Checklist final

- [ ] Todos os nomes de arquivo sem acento, sem espaço e em minúsculas
- [ ] Logos e diagramas em SVG, com contornos convertidos
- [ ] Fotos em JPG, até 2.000 px e 500 KB
- [ ] As 3 cores de cada assinatura (colorida, positivo, negativo)
- [ ] Pacotes `.zip` de download, um por versão e formato
- [ ] Fontes: `.zip` + licença (+ `.woff2` para exibir no manual)
- [ ] Ficha de dados preenchida e passada para o `brand.js`
- [ ] Versões que não existem avisadas, para remover do `brand.js`
- [ ] Manual aberto no navegador para conferir se não sobrou placeholder cinza
