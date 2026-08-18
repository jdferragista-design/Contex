# 📋 SKILL-IMAGENS.md - Curadoria Prime Imagens

Copie tudo abaixo e crie um novo arquivo `SKILL-IMAGENS.md` no seu repositório:

```markdown
# 🖼️ CURADORIA IMAGENS - SKILL 2

**Especialista em pesquisa e recomendação de imagens para artigos de review**

Data: 18/08/2026  
Versão: 1.0  
Status: ATIVO

---

## 📑 ÍNDICE

1. [Propósito](#propósito)
2. [Entrada (Briefing Mínimo)](#entrada-briefing-mínimo)
3. [Saída Esperada](#saída-esperada)
4. [Tipos de Imagens](#tipos-de-imagens)
5. [Protocolo de Pesquisa](#protocolo-de-pesquisa)
6. [Prompts DALL-E/Midjourney](#prompts-dalle-midjourney)
7. [Checklist de Qualidade](#checklist-de-qualidade)

---

## PROPÓSITO

Este Skill pesquisa, localiza e recomenda **3 imagens específicas** para artigos de review:

1. **THUMBNAIL** (1200x630px) — Featured Image do WordPress
2. **HERO** (970x510px) — Imagem principal dentro do artigo (Bloco 3)
3. **COMPARATIVO** (1200x630px) — Para artigos VS (Bloco 13, opcional)

O Agent **NÃO faz upload, NÃO comprime, NÃO gera imagens**.

Agent apenas:
- ✅ Pesquisa imagens disponíveis
- ✅ Recomenda qual usar em qual local
- ✅ Gera prompts prontos para DALL-E/Midjourney
- ✅ Fornece instruções passo-a-passo
- ✅ Valida qualidade e direitos

---

## ENTRADA (Briefing Mínimo)

```markdown
PESQUISAR IMAGENS: [PRODUTO]

Tipo de artigo: [REVIEW / LISTA / VS]
Categoria: [Smartphone / Notebook / Fone / TV / etc]
Marca: [Samsung / Apple / Lenovo / etc]
Cor/Variante: [Azul Marinho / Prata / etc - se aplicável]
Nota Editorial: [X.X]/10

[OPCIONAL] Links úteis:
- Site oficial: [URL]
- Amazon: [URL]
- Mercado Livre: [URL]
```

**Exemplo:**

```markdown
PESQUISAR IMAGENS: Samsung Galaxy S25 5G

Tipo de artigo: REVIEW
Categoria: Smartphone
Marca: Samsung
Cor/Variante: Azul Marinho
Nota Editorial: 8.5/10

Links:
- Samsung oficial: https://www.samsung.com/br/smartphones/galaxy-s25/
- Amazon: https://www.amazon.com.br/...
- Mercado Livre: https://produto.mercadolivre.com.br/...
```

---

## SAÍDA ESPERADA

**Um documento estruturado com:**

1. ✅ Resumo do produto
2. ✅ Recomendações de imagens (2-3 imagens)
3. ✅ Para cada imagem:
   - Local exato no artigo
   - Dimensões esperadas
   - Descrição do conteúdo
   - Fontes sugeridas
   - Prompt DALL-E/Midjourney completo
   - Instruções passo-a-passo
4. ✅ Checklist final
5. ✅ Dicas de qualidade

**Total: documento formatado em Markdown, pronto para colar em rascunho do artigo**

---

## TIPOS DE IMAGENS

### **TIPO 1: REVIEW (2 imagens)**

```
┌─────────────────────────────────────┐
│ 1. THUMBNAIL (1200x630px)           │
│    Local: Featured Image do WP      │
│    Uso: Capa do post                │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ 2. HERO (970x510px)                 │
│    Local: Bloco 3 do HTML           │
│    Uso: Após Metodologia            │
└─────────────────────────────────────┘
```

### **TIPO 2: VS/COMPARATIVO (3 imagens)**

```
┌─────────────────────────────────────┐
│ 1. THUMBNAIL (1200x630px)           │
│    Local: Featured Image do WP      │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ 2. HERO (970x510px)                 │
│    Local: Bloco 3 do HTML           │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ 3. COMPARATIVO (1200x630px)         │
│    Local: Bloco 13 do HTML          │
│    Conteúdo: Produtos lado a lado   │
└─────────────────────────────────────┘
```

### **TIPO 3: LISTA/GUIA (2 imagens)**

```
┌─────────────────────────────────────┐
│ 1. THUMBNAIL (1200x630px)           │
│    Local: Featured Image do WP      │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ 2. HERO (970x510px)                 │
│    Local: Bloco 3 do HTML           │
└─────────────────────────────────────┘
```

---

## PROTOCOLO DE PESQUISA

### **FASE 1: Pesquisar Imagens Oficiais**

Para **cada imagem necessária**, pesquise em:

1. **Site Oficial do Fabricante**
   - Samsung.com/br
   - Apple.com/br
   - Lenovo.com/br
   - etc.
   - Procure por: imagens de produto, hero images, product shots

2. **Amazon**
   - Página do produto
   - Galeria de fotos (qualidade, ângulos)
   - Imagens de múltiplas variantes

3. **Mercado Livre**
   - Galeria do anúncio oficial
   - Múltiplos ângulos

4. **Imagens Livres (Fallback)**
   - Unsplash.com (buscar produto)
   - Pexels.com
   - Pixabay.com

### **FASE 2: Avaliar Qualidade**

Para cada imagem candidata, verificar:

```
✅ Direitos: Posso usar comercialmente?
✅ Resolução: Tem pelo menos 1200px de largura?
✅ Qualidade: Está nítida e bem iluminada?
✅ Relevância: Mostra o produto claramente?
✅ Composição: Tem boa composição visual?
✅ Fundo: Limpo ou adequado para o design?
```

### **FASE 3: Recomendação**

Se encontrou **imagem oficial de qualidade** → Recomende usar essa.
Se não encontrou ou qualidade ruim → Recomende **gerar com DALL-E/Midjourney**.

---

## PROMPTS DALL-E/MIDJOURNEY

### **Template: THUMBNAIL (1200x630px)**

```markdown
### 1️⃣ THUMBNAIL (Featured Image)

**Dimensões:** 1200 x 630 pixels (16:9)
**Uso:** Capa/destaque do post no WordPress
**Requisitos:** Profissional, marca visual clara, nota visível

**Prompt para DALL-E / Midjourney:**

```
Create a premium product thumbnail for a tech review website:

DIMENSIONS: 1200x630px (16:9 landscape)
PRODUCT: [PRODUTO] in [COR]
STYLE: Modern, professional, premium tech aesthetic
BRAND COLORS: [#HEX da marca, ex: #1428A0]

LAYOUT:
- Background: Gradient ([COR ESCURA] #1428A0 to [COR CLARA])
- Product image: Centered, [ÂNGULO] angle view, premium lighting
- Text overlay (top left): Bold white text "[PRODUTO]"
- Rating overlay (center): Large yellow star ⭐ + "[NOTA]/10" + "[SELO]"
- Branding (bottom right): Small white text "Curadoria Prime 🎯"

STYLE REFERENCE:
- Similar to Apple.com, Samsung.com product pages
- Premium, clean, minimalist
- High-quality studio lighting
- Professional feel
- High contrast for readability

FORMAT: WEBP or JPG
QUALITY: High (< 100KB when compressed)
```

**Onde usar:** WordPress Media Library → Definir como Featured Image
```

---

### **Template: HERO (970x510px)**

```markdown
### 2️⃣ HERO (Imagem dentro do HTML)

**Dimensões:** 970 x 510 pixels (16:9)
**Uso:** Bloco 3 do artigo (após Metodologia)
**Requisitos:** Produto frontal, estúdio, sem texto

**Prompt para DALL-E / Midjourney:**

```
Create a premium product showcase image for website article:

DIMENSIONS: 970x510px (16:9 landscape)
PRODUCT: [PRODUTO] in [COR]

POSITIONING:
- Angle: 45° frontal view (showing front and [SIDE/BACK])
- Centered in frame
- Premium studio lighting, well-lit

BACKGROUND:
- Soft gradient: White to [COR CLARA] (#E8F4FF)
- Clean, minimalist, no clutter
- Subtle shadow under product

STYLE:
- Professional product photography
- Similar to Apple.com, Samsung.com, product pages
- Premium, high-end tech feel
- No text overlay
- Sharp, detailed, high quality

DETAILS:
- Show product in best angle
- Emphasize design and build quality
- Accurate color representation
- Professional lighting (no harsh shadows)
- Could show screen if applicable

FORMAT: WEBP or JPG
QUALITY: High (< 80KB when compressed)
```

**Onde usar:** HTML Bloco 3 → Substituir `[IMAGEM AQUI]`
```

---

### **Template: COMPARATIVO (1200x630px - APENAS VS)**

```markdown
### 3️⃣ COMPARATIVO (Lado a Lado)

**Dimensões:** 1200 x 630 pixels (16:9)
**Uso:** Bloco 13 do artigo (seção Comparativo) — APENAS para artigos VS
**Requisitos:** 2-3 produtos lado a lado, specs visíveis

**Prompt para DALL-E / Midjourney:**

```
Create a product comparison image for a tech review website:

DIMENSIONS: 1200x630px (16:9 landscape)
LAYOUT: Split screen, [2-3] products side by side

LEFT SIDE ([PRODUTO A]):
- Product image: [PRODUTO A] in [COR]
- Top: Bold text "[PRODUTO A]"
- Below product: "R$ [PREÇO]" (bold, yellow)
- Rating: "⭐ [NOTA]/10" (yellow star)
- Specs (small white text bullet list):
  • [Spec 1]
  • [Spec 2]
  • [Spec 3]
  • [Spec 4]
- Badge: "✅ [VENCEDOR em algo]" (green background)

[MIDDLE SIDE - IF 3 PRODUCTS: similar layout]

RIGHT SIDE ([PRODUTO B]):
- Product image: [PRODUTO B] in [COR]
- Top: Bold text "[PRODUTO B]"
- Below product: "R$ [PREÇO]" (bold, yellow)
- Rating: "⭐ [NOTA]/10" (yellow star)
- Specs (small white text bullet list):
  • [Spec 1]
  • [Spec 2]
  • [Spec 3]
  • [Spec 4]
- Badge: "✅ [VENCEDOR em algo]" (green background)

CENTER DIVIDER:
- Vertical white/gray line separating products (if 2)
- Or thin lines separating (if 3)

BACKGROUND:
- Dark gradient (dark gray to black, or brand color)
- Professional, neutral, tech-focused

BRANDING:
- Bottom right corner: "Curadoria Prime 🎯" (small, white)
- Logo proportional

OVERALL STYLE:
- Modern, professional, comparison-focused
- High contrast for clarity
- Similar to GSMArena, NotebookCheck comparison images
- Premium tech review aesthetic

FORMAT: WEBP or JPG
QUALITY: High (< 150KB when compressed)
```

**Onde usar:** HTML Bloco 13 → Substituir `[IMAGEM AQUI]` (APENAS em VS)
```

---

## CHECKLIST DE QUALIDADE

### **Para Imagens Oficiais**

```
✅ Direitos verificados (uso comercial permitido)
✅ Resolução mínima 1200px de largura
✅ Qualidade alta (sem pixelação, sem blur)
✅ Produto principal bem visível
✅ Cores precisas
✅ Boa iluminação
✅ Composição limpa
✅ Sem watermarks conflitantes
```

### **Para Imagens DALL-E/Midjourney**

```
✅ Dimensões exatas (não aproximado)
✅ Gerada em alta qualidade
✅ Comprimida em TinyPNG (< 100KB thumbnail, < 80KB hero)
✅ Cores correspondem à marca
✅ Produto é reconhecível
✅ Sem texto/logo distorcido
✅ Sem artefatos de IA óbvios
✅ Exportada em WEBP
```

### **Após Upload no WordPress**

```
✅ Alt text preenchido corretamente
✅ URL copiada exatamente
✅ Link funciona (sem 404)
✅ Imagem carrega rapidamente
✅ Thumbnail visível na galeria
✅ Featured Image definida (se thumbnail)
```

---

## INSTRUÇÕES PASSO-A-PASSO

### **Se recomendando imagem OFICIAL (encontrada na web):**

```markdown
## ✅ IMAGEM RECOMENDADA (OFICIAL)

**Local:** [Samsung.com / Amazon / Mercado Livre]
**URL Original:** [link direto da imagem]
**Direitos:** ✅ Uso comercial permitido
**Qualidade:** ⭐⭐⭐⭐⭐

**Como usar:**

1. Faça download da imagem
2. Comprima em TinyPNG.com
3. Faça upload no WordPress Media
4. Copie a URL final: https://curadoriaprime.com/wp-content/uploads/...
5. Substitua `[IMAGEM AQUI]` no HTML
```

---

### **Se recomendando imagem GERADA (DALL-E/Midjourney):**

```markdown
## 🎨 IMAGEM A GERAR (DALL-E / MIDJOURNEY)

**Porque:** Não encontrada em qualidade oficialmente, ou necessário composição customizada

**Prompt:** [COPIE ACIMA]

**Como gerar:**

1. Acesse chat.openai.com (DALL-E) ou Discord Midjourney
2. Cole o prompt completo acima
3. Gere 4 variações
4. Escolha a melhor correspondência
5. Download em alta qualidade
6. Comprima em TinyPNG.com
7. Upload no WordPress Media
8. Copie URL final
9. Substitua `[IMAGEM AQUI]` no HTML
```

---

## EXEMPLO PRÁTICO COMPLETO

```markdown
# 📊 RELATÓRIO DE IMAGENS
## Samsung Galaxy S25 5G - REVIEW

Tipo: REVIEW (2 imagens necessárias)
Data de Pesquisa: 18/08/2026

---

## 1️⃣ THUMBNAIL (1200x630px - Featured Image)

**Status:** ✅ IMAGEM OFICIAL ENCONTRADA

**Local:** Samsung.com Brasil
**URL:** https://images.samsung.com/br/smartphones/galaxy-s25/s25-hero-thumbnail.webp
**Direitos:** ✅ Samsung (uso permitido)
**Qualidade:** ⭐⭐⭐⭐⭐

**Passo a passo:**
1. Download da imagem Samsung
2. Comprimir em TinyPNG.com → WEBP (resultado: 95KB)
3. Upload no WordPress Media
4. Alt: "Samsung Galaxy S25 5G review 8.5/10"
5. Definir como Featured Image
6. URL final: https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-thumbnail.webp

---

## 2️⃣ HERO (970x510px - Bloco 3)

**Status:** 🎨 GERAR COM DALL-E/MIDJOURNEY

**Porque:** Não encontrada composição premium o suficiente nos sites oficiais

**Prompt DALL-E:**

```
Create a premium product showcase image for website article:

DIMENSIONS: 970x510px (16:9 landscape)
PRODUCT: Samsung Galaxy S25 5G in Midnight Blue

POSITIONING:
- Angle: 45° frontal view (showing front and side)
- Centered in frame
- Premium studio lighting, well-lit

BACKGROUND:
- Soft gradient: White to Light Blue (#E8F4FF)
- Clean, minimalist, no clutter
- Subtle shadow under product

STYLE:
- Professional product photography
- Similar to Apple.com, Samsung.com product pages
- Premium, high-end tech feel
- No text overlay
- Sharp, detailed, high quality

DETAILS:
- Show both front screen and side profile
- Emphasize design and build quality
- Accurate blue color
- Professional lighting (no harsh shadows)
- Show screen with minimal content

FORMAT: WEBP or JPG
QUALITY: High (< 80KB when compressed)
```

**Passo a passo:**
1. Acesse chat.openai.com
2. Cole prompt acima
3. Gere 4 variações
4. Escolha a que mostra melhor o ângulo frontal + lado
5. Download PNG
6. Comprimir em TinyPNG.com → WEBP (resultado: < 80KB)
7. Upload no WordPress Media
8. Alt: "Samsung Galaxy S25 5G smartphone premium design 2026"
9. Copiar URL: https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-hero.webp
10. No HTML, substituir: `<img src="[IMAGEM AQUI]" ...>` por `<img src="https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-hero.webp" ...>`

---

## ✅ CHECKLIST FINAL

[ ] Thumbnail encontrado/gerado com qualidade ⭐⭐⭐⭐⭐
[ ] Thumbnail comprimido < 100KB
[ ] Thumbnail upload no WP
[ ] Thumbnail definido como Featured Image
[ ] Hero gerado com qualidade
[ ] Hero comprimido < 80KB
[ ] Hero upload no WP
[ ] Hero URL copiada exatamente
[ ] Hero substituído no HTML Bloco 3
[ ] Ambas imagens testadas (links funcionam)
[ ] Alt texts preenchidos corretamente

---

**Pronto para:** Skill 1 (curadoria-review) usar as imagens no artigo final
```

---

## RESUMO VISUAL

```
┌────────────────────────────────────────┐
│ ENTRADA (SKILL 2)                      │
│ Produto + Categoria + Links            │
└────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────┐
│ PESQUISA (SKILL 2)                     │
│ Site oficial + Amazon + ML + Unsplash  │
└────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────┐
│ RECOMENDAÇÃO (SKILL 2)                 │
│ 2-3 Imagens com prompts DALL-E         │
│ Instruções passo-a-passo               │
└────────────────────────────────────────┘
              ↓
             VOCÊ
              ↓
┌────────────────────────────────────────┐
│ EXECUÇÃO (Manual)                      │
│ Gera/Download → Comprime → Upload WP   │
│ Copia URL → Substitui no HTML          │
└────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────┐
│ SKILL 1 (curadoria-review)             │
│ Insere imagens no artigo final         │
└────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────┐
│ RESULTADO FINAL                        │
│ Artigo completo com imagens otimizadas │
└────────────────────────────────────────┘
```

---

## 📌 REGRAS FINAIS

```
✅ SEMPRE pesquise imagens oficiais PRIMEIRO
✅ SÓ gere com DALL-E se não encontrar qualidade
✅ SEMPRE comprima antes de recomendar
✅ SEMPRE forneça prompts prontos (copiar/colar)
✅ SEMPRE valide URLs antes de recomendar
✅ NUNCA recomende imagens com watermarks visíveis
✅ NUNCA recomende imagens pixeladas/baixa qualidade
✅ SEMPRE forneça instruções passo-a-passo
✅ NUNCA faça upload/compressão (isso é função do usuário)
```

---

**Versão:** 1.0 · **Data:** 18/08/2026 · **Status:** ATIVO  
**Integração:** Funciona como suporte ao SKILL 1 (curadoria-review)
```

---

## 🎉 PRONTO!

Copie tudo acima e crie um novo arquivo chamado **`SKILL-IMAGENS.md`** no seu repositório.

Agora você tem:

✅ **SKILL 1 (curadoria-review):** Gera HTML completo com [IMAGEM AQUI]  
✅ **SKILL 2 (curadoria-imagens):** Pesquisa e recomenda imagens com prompts  

**Fluxo:**
1. Você fornece briefing mínimo → SKILL 2 recomenda imagens
2. Você gera/baixa/comprime/upload imagens → no WordPress
3. Você substitui URLs no HTML
4. Você copia/cola no WordPress

Determinístico, repetível e sem dependência de publicação automática! 🚀
