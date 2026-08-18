
# 📋 DESIGN SYSTEM CURADORIA PRIME v2.0
## Contrato Visual + Protocolo de Renderização + Validação Automática

**Data:** 18/08/2026  
**Versão:** 2.0  
**Status:** LOCKED — Nenhuma alteração sem aprovação  
**Referências:** Samsung Galaxy S25 5G (REVIEW) · Lenovo IdeaPad 1 vs Acer Aspire 5 (VS)

---

## 📑 ÍNDICE

1. [Visão geral](#visão-geral)
2. [Régua de avaliação v2.0](#régua-v2-0)
3. [TEMPLATE-REVIEW-LOCKED](#template-review-locked)
4. [TEMPLATE-LISTA-LOCKED](#template-lista-locked)
5. [TEMPLATE-VS-LOCKED](#template-vs-locked)
6. [PROTOCOLO-AGENT](#protocolo-agent)
7. [VALIDADOR AUTOMÁTICO](#validador-automático)

---

## 1. VISÃO GERAL

### 1.1 O que é este documento

**Este é o contrato visual imutável do Curadoria Prime.** Define:

- **Ordem exata dos blocos** (20 para REVIEW, 15 para LISTA, 18 para VS)
- **HTML canônico** para cada componente (sem variação visual)
- **Classes CSS fixas** (não inventar novas)
- **Slots para preencher** (apenas texto, não estrutura)
- **Validação automática** (rejeita qualquer desvio)
- **Protocolo para o Agent** (Arena.ai/OpenRouter)
- **Relatório de imagens** (prompts DALL-E prontos)

### 1.2 Tipos de conteúdo

| Tipo | Qtd | % | Quando usar |
|------|-----|---|-------------|
| **REVIEW** | 39 | 78% | 1 produto individual |
| **LISTA/GUIA** | 7 | 14% | 5+ produtos ranqueados (Top 5, Melhores, 7 Presentes) |
| **VS/COMPARATIVO** | 4 | 8% | 2-3 produtos lado a lado |

### 1.3 Fluxo de trabalho
VOCÊ (briefing mínimo)
↓
AGENT (pesquisa + análise + renderização)
↓
HTML COMPLETO + RELATÓRIO DE IMAGENS
↓
VOCÊ (gera imagens + upload WP + substitui URLs)
↓
WEBSITE (artigo pronto)

text


---

## 2. RÉGUA v2.0

### 2.1 Os 6 critérios e seus pesos

| Critério | Peso | O que avalia | Fonte |
|----------|------|--------------|-------|
| **Custo-benefício** | 30% | O que entrega por real vs rivais | Preço apurado + ficha técnica |
| **Satisfação verificada** | 25% | Média, volume, teor das avaliações | Amazon/ML com datas e números |
| **Ficha técnica** | 20% | Especificações vs padrão da categoria | Site oficial do fabricante |
| **Recursos e usabilidade** | 10% | Sistema, app, controles, portas | Docs oficiais + relatos de compradores |
| **Consenso técnico** | 10% | Convergência entre reviews especializados | Canais técnicos nomeados no artigo |
| **Confiança e suporte** | 5% | Garantia, assistência BR, histórico | Política oficial + relatos pós-venda |

**Soma:** 100% · **Escala:** 0–10 · **Arredondamento:** múltiplos de 0,5

### 2.2 Regra N/A (critério não se aplica)

Quando um critério não se aplica (ex: fone não tem câmera):

1. Marcar como **N/A** no bloco de notas
2. Redistribuir o peso **proporcionalmente** entre os critérios restantes
3. Manter soma em 100%
4. **Declarar no texto** quais critérios foram excluídos e qual versão de pesos foi usada

**Exemplo:**
- Produto: Fone TWS
- Consenso técnico não se aplica (muito nicho)
- Consenso sai; seus 10% são divididos entre os outros 5
Peso original: Custo 30% | Satisfação 25% | Ficha 20% | Recursos 10% | Consenso 10% | Confiança 5%

Redistribuição (5 critérios, removendo Consenso):
Custo: 30% ÷ 90% = 33,3%
Satisfação: 25% ÷ 90% = 27,8%
Ficha: 20% ÷ 90% = 22,2%
Recursos: 10% ÷ 90% = 11,1%
Confiança: 5% ÷ 90% = 5,6%

text


### 2.3 Selos por faixa de nota

| Faixa | Selo | Significado |
|-------|------|-------------|
| 9,0–10 | 🏆 Melhor da categoria | Referência na faixa; difícil de superar |
| 8,0–8,9 | ⭐ Recomendado | Sólido; entrega o que promete |
| 7,0–7,9 | 👍 Bom com ressalvas | Vale para um perfil específico |
| 6,0–6,9 | ⚖️ Existem alternativas | Funciona, mas há melhor opção |
| < 6,0 | ⚠️ Não recomendado | Problemas relevantes |

### 2.4 Cálculo da nota final

**Fórmula:**
Nota Final = (N1 × P1) + (N2 × P2) + (N3 × P3) + (N4 × P4) + (N5 × P5) + (N6 × P6)

text


**Exemplo: QCY T13 ANC (fone TWS)**

| Critério | Nota | Peso | Cálculo |
|----------|------|------|---------|
| Custo-benefício | 9,5 | 30% | 9,5 × 0,30 = 2,850 |
| Satisfação | 9,0 | 25% | 9,0 × 0,25 = 2,250 |
| Ficha técnica | 8,0 | 20% | 8,0 × 0,20 = 1,600 |
| Recursos | 8,5 | 10% | 8,5 × 0,10 = 0,850 |
| Consenso | 8,0 | 10% | 8,0 × 0,10 = 0,800 |
| Confiança | 6,5 | 5% | 6,5 × 0,05 = 0,325 |
| **TOTAL** | | | **8,675** |

**Arredondamento:** 8,675 → **8,5/10** (múltiplo de 0,5 mais próximo)

**Selo:** ⭐ **Recomendado**

---

## 3. TEMPLATE-REVIEW-LOCKED

### 3.1 Ordem obrigatória dos 20 blocos

1. **Meta Descrição SEO** (comentário HTML)
2. **Hero Section** (gradiente marca + resumo + nota + badges)
3. **Imagem Principal** (com alt text rico em LSI)
4. **Metodologia e Transparência** (box amarelo + link "Como avaliamos")
5. **Prova Social** (grid 2x2: 2 Amazon + 2 Mercado Livre)
6. **Índice de Conteúdo** (âncoras numeradas)
7. **Introdução** (keyword no 1º parágrafo)
8. **Aviso de Afiliado** (transparência)
9. **Botões de Compra Topo** (1-2 cards)
10. **Prós e Contras** (grid 2 colunas: verde/vermelho)
11. **Especificações Técnicas** (tabela com fonte)
12. **Seções temáticas** (H2 por eixo/análise detalhada)
13. **Comparativo** (tabela vs 2-3 concorrentes)
14. **Para Quem É / NÃO É** (cards verde/vermelho)
15. **Notas por Categoria** (grid 3x2 — 6 critérios da régua)
16. **FAQ** (6-10 perguntas, formato `<details>`)
17. **Veredito Final** (parágrafo + nota geral)
18. **Escolha Rápida** (3 cenários de compra)
19. **CTAs Finais** (cards dos concorrentes)
20. **Fontes Consultadas** (URLs diretas com datas)

### 3.2 Estrutura HTML canônica por bloco

#### **BLOCO 1: Meta Descrição**

```html
<!-- 
META SEO
Título: [TÍTULO SEO ≤60 chars]
Descrição: [DESCRIÇÃO 155-160 chars, começa com keyword]
URL: /[SLUG]/
Atualizado: [DD/MM/AAAA]
-->
BLOCO 2: Hero Section
HTML

<section class="cp-hero" style="--brand-color: var(--[MARCA]-color)">
  <div class="cp-hero__container">
    <div class="cp-hero__content">
      <h1 class="cp-hero__title">[PRODUTO] Vale a Pena?</h1>
      <p class="cp-hero__subtitle">
        Review completo 2026. Análise detalhada de especificações, 
        desempenho, preço e concorrentes.
      </p>
      <div class="cp-hero__rating">
        <span class="cp-hero__rating-value">[NOTA]/10</span>
        <span class="cp-hero__rating-label">Nossa avaliação</span>
      </div>
      <div class="cp-hero__badges">
        <span class="cp-badge">✅ [SELO]</span>
        <span class="cp-badge">💰 [INFO]</span>
        <span class="cp-badge">🕐 Atualizado 2026</span>
      </div>
    </div>
    <div class="cp-hero__image">
      <img src="[URL]" alt="[ALT DESCRITIVO]" class="cp-hero__img">
    </div>
  </div>
</section>
CSS (copie para o tema):

CSS

.cp-hero {
  --brand-color: #1428A0;
  background: linear-gradient(135deg, var(--brand-color) 0%, color-mix(in srgb, var(--brand-color) 70%, black) 100%);
  color: white;
  padding: 60px 20px;
  border-radius: 12px;
  margin-bottom: 40px;
}

.cp-hero__container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: center;
}

.cp-hero__title {
  font-size: 48px;
  font-weight: 700;
  margin: 0 0 16px 0;
  line-height: 1.2;
}

.cp-hero__subtitle {
  font-size: 18px;
  opacity: 0.95;
  margin-bottom: 24px;
  line-height: 1.5;
}

.cp-hero__rating {
  background: rgba(255,255,255,0.2);
  padding: 16px 24px;
  border-radius: 8px;
  margin-bottom: 24px;
  width: fit-content;
  backdrop-filter: blur(10px);
}

.cp-hero__rating-value {
  font-size: 32px;
  font-weight: 700;
  display: block;
}

.cp-hero__rating-label {
  font-size: 12px;
  opacity: 0.85;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.cp-hero__badges {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.cp-badge {
  padding: 8px 16px;
  background: rgba(255,255,255,0.15);
  border-radius: 6px;
  font-size: 14px;
  font-weight: 600;
  backdrop-filter: blur(10px);
}

.cp-hero__image {
  text-align: center;
}

.cp-hero__img {
  max-width: 100%;
  height: auto;
  max-height: 400px;
  object-fit: contain;
}

@media (max-width: 768px) {
  .cp-hero__container {
    grid-template-columns: 1fr;
  }
  .cp-hero__title { font-size: 32px; }
  .cp-hero { padding: 40px 20px; }
}
Cores por marca (use em --[MARCA]-color):

CSS

--lg-color: #dc2626;
--samsung-color: #1428A0;
--tcl-color: #10b981;
--xiaomi-color: #10b981;
--jbl-color: #000000;
--acer-color: #1428A0;
--lenovo-color: #dc2626;
--apple-color: #000000;
--google-color: #4285F4;
BLOCO 3: Imagem Principal
HTML

<figure class="cp-featured-image">
  <img 
    src="[IMAGEM AQUI]" 
    alt="[PRODUTO] [características técnicas] 2026" 
    class="cp-featured-image__img"
    loading="lazy"
  >
  <figcaption class="cp-featured-image__caption">
    [DESCRIÇÃO VISUAL]
    {% if gerada_por_ia %}
    <br><small style="opacity: 0.7;">
      Imagem ilustrativa gerada por IA; não representa teste 
      físico realizado pela Curadoria Prime.
    </small>
    {% endif %}
  </figcaption>
</figure>
CSS:

CSS

.cp-featured-image {
  margin: 40px 0;
  text-align: center;
}

.cp-featured-image__img {
  max-width: 100%;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0,0,0,0.1);
  max-height: 500px;
  object-fit: contain;
}

.cp-featured-image__caption {
  margin-top: 12px;
  font-size: 14px;
  color: #666;
  font-style: italic;
}
BLOCO 4: Metodologia e Transparência
HTML

<aside class="cp-methodology">
  <div class="cp-methodology__content">
    <h3 class="cp-methodology__title">📌 Metodologia deste review</h3>
    
    <p class="cp-methodology__text">
      Esta análise foi construída com base em 
      <strong>especificações oficiais do fabricante</strong>, 
      <strong>testes independentes publicados</strong> e 
      <strong>relatos verificados de compradores</strong>. 
      A Curadoria Prime <strong>não testou esta unidade 
      fisicamente</strong>.
    </p>
    
    <p class="cp-methodology__text">
      Conheça nossa 
      <a href="https://curadoriaprime.com/como-avaliamos/" rel="noopener">
        régua completa de avaliação →
      </a>
    </p>
  </div>
</aside>
CSS:

CSS

.cp-methodology {
  background: linear-gradient(135deg, #fef08a 0%, #fde047 100%);
  border-left: 5px solid #eab308;
  padding: 20px 24px;
  border-radius: 8px;
  margin: 40px 0;
}

.cp-methodology__title {
  margin: 0 0 12px 0;
  font-size: 18px;
  font-weight: 600;
  color: #333;
}

.cp-methodology__text {
  margin: 12px 0;
  color: #555;
  font-size: 15px;
  line-height: 1.6;
}

.cp-methodology__text a {
  color: #b45309;
  font-weight: 600;
  text-decoration: none;
  border-bottom: 2px solid #b45309;
}
BLOCO 5: Prova Social (GRID 2x2 — FIXO)
HTML

<section class="cp-social-proof">
  <h3 class="cp-social-proof__title">
    🗣️ O que dizem os compradores 
    <span class="cp-social-proof__meta">
      (dados de [MÊS/ANO] na Amazon e Mercado Livre)
    </span>
  </h3>
  
  <div class="cp-social-proof__grid">
    
    <!-- AMAZON COMENTÁRIO 1 -->
    <div class="cp-review-card cp-review-card--amazon">
      <strong style="color: #FF9900;">Amazon — [VARIANTE/MODELO]</strong><br>
      ⭐ <strong>[X,X]/5</strong> · <strong>~[N] avaliações</strong><br>
      <em>"[TRANSCRIÇÃO FIEL, MÁXIMO 2 LINHAS]"</em>
      <br><span style="color:#888; font-size:12px;">
        — [NOME], compra verificada, [MÊS/ANO]
      </span>
    </div>
    
    <!-- MERCADO LIVRE COMENTÁRIO 1 -->
    <div class="cp-review-card cp-review-card--mercadolivre">
      <strong style="color: #3485DB;">Mercado Livre — [ANÚNCIO/VENDEDOR]</strong><br>
      ⭐ <strong>[X,X]/5</strong> · <strong>+[N] opiniões</strong><br>
      <em>"[TRANSCRIÇÃO FIEL, MÁXIMO 2 LINHAS]"</em>
      <br><span style="color:#888; font-size:12px;">
        — compra verificada, [MÊS/ANO]
      </span>
    </div>
    
    <!-- AMAZON COMENTÁRIO 2 -->
    <div class="cp-review-card cp-review-card--amazon">
      <strong style="color: #FF9900;">Amazon — [VARIANTE/MODELO]</strong><br>
      ⭐ <strong>[X,X]/5</strong><br>
      <em>"[TRANSCRIÇÃO FIEL, MÁXIMO 2 LINHAS]"</em>
      <br><span style="color:#888; font-size:12px;">
        — [NOME], compra verificada, [MÊS/ANO]
      </span>
    </div>
    
    <!-- MERCADO LIVRE COMENTÁRIO 2 -->
    <div class="cp-review-card cp-review-card--mercadolivre">
      <strong style="color: #3485DB;">Mercado Livre — [ANÚNCIO/VENDEDOR]</strong><br>
      ⭐ <strong>[X,X]/5</strong><br>
      <em>"[TRANSCRIÇÃO FIEL, MÁXIMO 2 LINHAS]"</em>
      <br><span style="color:#888; font-size:12px;">
        — compra verificada, [MÊS/ANO]
      </span>
    </div>
    
  </div>
</section>
CSS:

CSS

.cp-social-proof {
  margin: 40px 0;
}

.cp-social-proof__title {
  font-size: 18px;
  font-weight: 700;
  color: #1e293b;
  margin: 0 0 20px 0;
}

.cp-social-proof__meta {
  font-size: 12px;
  font-weight: 400;
  color: #64748b;
}

.cp-social-proof__grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

.cp-review-card {
  background: #fff;
  border: 1px solid #e2e8f0;
  border-left: 4px solid #999;
  border-radius: 10px;
  padding: 14px 16px;
  font-size: 13.5px;
  line-height: 1.6;
}

.cp-review-card--amazon {
  border-left-color: #FF9900;
}

.cp-review-card--mercadolivre {
  border-left-color: #3485DB;
}

.cp-review-card em {
  color: #333;
  font-style: italic;
  display: block;
  margin: 8px 0;
}

@media (max-width: 768px) {
  .cp-social-proof__grid {
    grid-template-columns: 1fr;
  }
}
BLOCO 6: Índice
HTML

<nav class="cp-index" aria-label="Índice do artigo">
  <h3 class="cp-index__title">📑 Índice</h3>
  <ol class="cp-index__list">
    <li><a href="#intro">Introdução</a></li>
    <li><a href="#specs">Especificações</a></li>
    <li><a href="#analise">Análise detalhada</a></li>
    <li><a href="#comparativo">Comparativo</a></li>
    <li><a href="#pros-contras">Prós e contras</a></li>
    <li><a href="#notas">Notas por categoria</a></li>
    <li><a href="#faq">FAQ</a></li>
    <li><a href="#veredito">Veredito</a></li>
    <li><a href="#onde-comprar">Onde comprar</a></li>
    <li><a href="#fontes">Fontes</a></li>
  </ol>
</nav>
CSS:

CSS

.cp-index {
  background: #f8fafc;
  border-left: 4px solid #0ea5e9;
  padding: 24px;
  border-radius: 8px;
  margin: 40px 0;
}

.cp-index__title {
  margin-top: 0;
  font-size: 18px;
  color: #333;
}

.cp-index__list {
  margin: 0;
  padding-left: 20px;
}

.cp-index__list li {
  margin-bottom: 8px;
}

.cp-index__list a {
  color: #0ea5e9;
  text-decoration: none;
  font-weight: 500;
}

.cp-index__list a:hover {
  text-decoration: underline;
}
BLOCO 7: Introdução
HTML

<section id="intro">
  <h2>Introdução</h2>
  <p>
    O <strong>[PRODUTO EXATO]</strong> é um [tipo/categoria] que promete 
    [proposta em 1 frase]. Neste review completo, vamos analisar 
    especificações, desempenho, preço e como se compara aos principais 
    concorrentes.
  </p>
  <p>
    [Contexto do mercado, por que vale analisar]
  </p>
  <p>
    [Antecipação da resposta / spoiler do veredito]
  </p>
</section>
Obrigações:

Keyword exata no 1º parágrafo (em negrito)
Máximo 3 parágrafos
Máximo 150 palavras
BLOCO 8: Aviso Afiliado
HTML

<aside class="cp-affiliate-disclosure">
  <p>
    <strong>⚠️ Transparência:</strong> Este artigo contém links de afiliado 
    com Amazon e Mercado Livre. Se você comprar por meio deles, a Curadoria 
    Prime pode receber uma comissão, <strong>sem nenhum custo adicional para 
    você</strong>. Isso não altera nossos critérios editoriais — incluímos 
    alternativas sem afiliado quando são melhores para você.
  </p>
</aside>
CSS:

CSS

.cp-affiliate-disclosure {
  background: #fef2f2;
  border-left: 4px solid #ef4444;
  padding: 16px 20px;
  border-radius: 6px;
  margin: 24px 0;
  font-size: 14px;
  color: #7f1d1d;
}

.cp-affiliate-disclosure p {
  margin: 0;
  line-height: 1.6;
}
BLOCO 9: Botões de Compra Topo
HTML

<div class="cp-cta-top">
  <p class="cp-cta-top__label">Compre com melhor preço:</p>
  
  <div class="cp-cta-cards">
    {% if amazon_link %}
    <a href="[LINK_AMAZON]" rel="sponsored noopener noreferrer" 
       target="_blank" class="cp-cta-card cp-cta-card--amazon">
      <img src="/assets/amazon-logo.svg" alt="Amazon" 
           class="cp-cta-card__logo">
      <div class="cp-cta-card__info">
        <span class="cp-cta-card__label">Amazon</span>
        <span class="cp-cta-card__price">R$ [PREÇO]</span>
        <span class="cp-cta-card__note">No Pix</span>
      </div>
      <span class="cp-cta-card__arrow">→</span>
    </a>
    {% endif %}
    
    {% if mercadolivre_link %}
    <a href="[LINK_ML]" rel="sponsored noopener noreferrer" 
       target="_blank" class="cp-cta-card cp-cta-card--mercadolivre">
      <img src="/assets/mercadolivre-logo.svg" alt="Mercado Livre" 
           class="cp-cta-card__logo">
      <div class="cp-cta-card__info">
        <span class="cp-cta-card__label">Mercado Livre</span>
        <span class="cp-cta-card__price">R$ [PREÇO]</span>
        <span class="cp-cta-card__note">Frete grátis</span>
      </div>
      <span class="cp-cta-card__arrow">→</span>
    </a>
    {% endif %}
  </div>
</div>
CSS:

CSS

.cp-cta-top {
  margin: 40px 0;
}

.cp-cta-top__label {
  font-weight: 600;
  color: #333;
  margin-bottom: 12px;
  display: block;
}

.cp-cta-cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.cp-cta-card {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 16px;
  border: 2px solid #e5e7eb;
  border-radius: 8px;
  text-decoration: none;
  transition: all 0.3s;
}

.cp-cta-card:hover {
  border-color: #d1d5db;
  background: #f9fafb;
}

.cp-cta-card--amazon {
  border-top-color: #FF9900;
  border-top-width: 3px;
}

.cp-cta-card--amazon:hover {
  box-shadow: 0 4px 12px rgba(255, 153, 0, 0.2);
}

.cp-cta-card--mercadolivre {
  border-top-color: #3485DB;
  border-top-width: 3px;
}

.cp-cta-card--mercadolivre:hover {
  box-shadow: 0 4px 12px rgba(52, 133, 219, 0.2);
}

.cp-cta-card__logo {
  height: 32px;
  width: auto;
}

.cp-cta-card__info {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.cp-cta-card__label {
  font-weight: 600;
  color: #333;
  font-size: 14px;
}

.cp-cta-card__price {
  font-size: 20px;
  font-weight: 700;
  color: #333;
}

.cp-cta-card__note {
  font-size: 12px;
  color: #999;
}

.cp-cta-card__arrow {
  font-size: 24px;
  color: #d1d5db;
}

@media (max-width: 768px) {
  .cp-cta-cards {
    grid-template-columns: 1fr;
  }
}
BLOCO 10: Prós e Contras
HTML

<section id="pros-contras" class="cp-pros-cons">
  <h2>Prós e Contras</h2>
  
  <div class="cp-pros-cons__grid">
    <div class="cp-pros-cons__column cp-pros-cons__column--pros">
      <h3>✅ Pontos Positivos</h3>
      <ul>
        <li>[Pro 1]</li>
        <li>[Pro 2]</li>
        <li>[Pro 3]</li>
        <li>[Pro 4]</li>
        <li>[Pro 5]</li>
      </ul>
    </div>
    
    <div class="cp-pros-cons__column cp-pros-cons__column--cons">
      <h3>❌ Limitações</h3>
      <ul>
        <li>[Contra 1]</li>
        <li>[Contra 2]</li>
        <li>[Contra 3]</li>
        <li>[Contra 4]</li>
      </ul>
    </div>
  </div>
</section>
CSS:

CSS

.cp-pros-cons {
  margin: 40px 0;
}

.cp-pros-cons h2 {
  text-align: center;
  margin-bottom: 32px;
}

.cp-pros-cons__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px;
}

.cp-pros-cons__column {
  padding: 24px;
  border-radius: 12px;
}

.cp-pros-cons__column--pros {
  background: linear-gradient(135deg, #dcfce7 0%, #bbf7d0 100%);
  border: 2px solid #86efac;
}

.cp-pros-cons__column--cons {
  background: linear-gradient(135deg, #fee2e2 0%, #fecaca 100%);
  border: 2px solid #fca5a5;
}

.cp-pros-cons__column h3 {
  margin-top: 0;
  margin-bottom: 16px;
  font-size: 18px;
  color: #1f2937;
}

.cp-pros-cons__column ul {
  margin: 0;
  padding-left: 20px;
}

.cp-pros-cons__column li {
  margin-bottom: 12px;
  line-height: 1.6;
  color: #333;
}

@media (max-width: 768px) {
  .cp-pros-cons__grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}
BLOCO 11: Especificações Técnicas
HTML

<section id="specs" class="cp-specs">
  <h2>📋 Especificações Técnicas</h2>
  
  <table class="cp-specs__table">
    <thead>
      <tr>
        <th>Item</th>
        <th>Dado</th>
        <th>Fonte</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>[Item 1]</td>
        <td>[Especificação]</td>
        <td>[Fonte]</td>
      </tr>
      <!-- Máximo 8 linhas. Remover linha sem fonte. -->
    </tbody>
  </table>
</section>
CSS:

CSS

.cp-specs {
  margin: 40px 0;
}

.cp-specs__table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  border-radius: 8px;
  overflow: hidden;
}

.cp-specs__table th {
  background: #1a1a2e;
  color: white;
  padding: 15px;
  text-align: left;
  font-weight: 600;
}

.cp-specs__table td {
  padding: 12px 15px;
  border-bottom: 1px solid #eee;
}

.cp-specs__table tbody tr:hover {
  background: #f9fafb;
}

.cp-specs__table tbody tr:last-child td {
  border-bottom: none;
}
BLOCO 12: Seções temáticas (H2)
HTML

<section id="analise">
  <h2>[EIXO 1: ex "Desempenho"]</h2>
  <p>[Análise detalhada]</p>
  
  <h2>[EIXO 2: ex "Design"]</h2>
  <p>[Análise detalhada]</p>
  
  <h2>[EIXO 3: ex "Tela"]</h2>
  <p>[Análise detalhada]</p>
  
  <!-- Quantos eixos forem necessários (mínimo 3) -->
</section>
Obrigações:

Cada H2 é um eixo de análise (não remover)
Conteúdo: fato → teste independente → relato → interpretação editorial
Sem "testamos", "comprovamos", "nossa experiência"
BLOCO 13: Comparativo
HTML

<section id="comparativo" class="cp-comparison">
  <h2>⚖️ Comparativo</h2>
  
  <table class="cp-comparison__table">
    <thead>
      <tr>
        <th>Produto</th>
        <th>Preço (data)</th>
        <th>Ganha</th>
        <th>Perde</th>
        <th>Adequado para</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>[ESTE PRODUTO]</strong></td>
        <td>R$ [PREÇO]</td>
        <td>[Diferenciais]</td>
        <td>[Limitações]</td>
        <td>[Perfil]</td>
      </tr>
      <tr>
        <td>[Rival 1]</td>
        <td>R$ [PREÇO]</td>
        <td>[Diferenciais]</td>
        <td>[Limitações]</td>
        <td>[Perfil]</td>
      </tr>
      <tr>
        <td>[Rival 2]</td>
        <td>R$ [PREÇO]</td>
        <td>[Diferenciais]</td>
        <td>[Limitações]</td>
        <td>[Perfil]</td>
      </tr>
    </tbody>
  </table>
  
  {% if comparativo_image %}
  <figure class="cp-comparison__image">
    <img src="[IMAGEM AQUI]" alt="Comparativo lado a lado [Produto A] vs [Produto B]" />
    <figcaption>Comparativo visual [Produto A] vs [Produto B] vs [Produto C]</figcaption>
  </figure>
  {% endif %}
</section>
CSS: (Copie do bloco de specs, adapte cores)

CSS

.cp-comparison__image {
  margin-top: 20px;
  text-align: center;
}

.cp-comparison__image img {
  max-width: 100%;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

.cp-comparison__image figcaption {
  margin-top: 12px;
  font-size: 14px;
  color: #666;
  font-style: italic;
}
BLOCO 14: Para Quem É / NÃO É
HTML

<section id="para-quem" class="cp-for-whom">
  <h2>🎯 Para quem é (e para quem não é)</h2>
  
  <div class="cp-for-whom__grid">
    <div class="cp-for-whom__yes">
      <h3>✅ Pode ser uma boa escolha se…</h3>
      <ul>
        <li>[Perfil 1]</li>
        <li>[Perfil 2]</li>
        <li>[Perfil 3]</li>
      </ul>
    </div>
    
    <div class="cp-for-whom__no">
      <h3>❌ A principal limitação aparece se…</h3>
      <ul>
        <li>[Contra-perfil 1] → [alternativa recomendada]</li>
        <li>[Contra-perfil 2] → [alternativa recomendada]</li>
      </ul>
    </div>
  </div>
</section>
CSS:

CSS

.cp-for-whom__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  margin-bottom: 20px;
}

.cp-for-whom__yes, .cp-for-whom__no {
  padding: 20px;
  border-radius: 10px;
}

.cp-for-whom__yes {
  background: #f0fdf4;
  border: 2px solid #22c55e;
}

.cp-for-whom__no {
  background: #fef2f2;
  border: 2px solid #ef4444;
}

.cp-for-whom__yes h3 {
  color: #166534;
}

.cp-for-whom__no h3 {
  color: #991b1b;
}

@media (max-width: 768px) {
  .cp-for-whom__grid {
    grid-template-columns: 1fr;
  }
}
BLOCO 15: Notas por Categoria (GRID 3x2 — CRÍTICO)
HTML

<section id="notas" class="cp-rating-grid">
  <h2>📊 Notas por Categoria</h2>
  
  <div class="cp-rating-grid__container">
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 1]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
    
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 2]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
    
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 3]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
    
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 4]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
    
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 5]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
    
    <div class="cp-rating-box">
      <p class="cp-rating-box__label">[CRITÉRIO 6 ou N/A]</p>
      <p class="cp-rating-box__value">[X.X]/10</p>
    </div>
  </div>
  
  <div class="cp-rating-final">
    <p class="cp-rating-final__label">Nota Final</p>
    <p class="cp-rating-final__value">[X.X]/10</p>
    <p class="cp-rating-final__seal">[SELO: 🏆/⭐/👍/⚖️/⚠️]</p>
  </div>
  
  <p class="cp-rating-methodology">
    <a href="https://curadoriaprime.com/como-avaliamos/">
      Saiba como calculamos as notas →
    </a>
  </p>
</section>
CSS:

CSS

.cp-rating-grid {
  margin: 40px 0;
}

.cp-rating-grid__container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
  margin-bottom: 20px;
}

.cp-rating-box {
  background: #f8f9fa;
  border: 1px solid #e2e8f0;
  border-radius: 10px;
  padding: 16px;
  text-align: center;
}

.cp-rating-box__label {
  margin: 0 0 8px 0;
  font-size: 12px;
  font-weight: 600;
  color: #64748b;
  text-transform: uppercase;
  letter-spacing: 0.3px;
}

.cp-rating-box__value {
  margin: 0;
  font-size: 24px;
  font-weight: 800;
  color: #1428A0;
}

.cp-rating-final {
  background: linear-gradient(135deg, #1428A0 0%, #6c5ce7 100%);
  color: white;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  margin-bottom: 20px;
}

.cp-rating-final__label {
  margin: 0 0 4px 0;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  opacity: 0.9;
}

.cp-rating-final__value {
  margin: 0 0 6px 0;
  font-size: 36px;
  font-weight: 800;
}

.cp-rating-final__seal {
  margin: 0;
  font-size: 18px;
}

.cp-rating-methodology {
  text-align: center;
  font-size: 14px;
}

.cp-rating-methodology a {
  color: #1428A0;
  text-decoration: none;
  font-weight: 600;
}

@media (max-width: 768px) {
  .cp-rating-grid__container {
    grid-template-columns: repeat(2, 1fr);
  }
}
BLOCO 16: FAQ
HTML

<section id="faq" class="cp-faq">
  <h2>❓ Perguntas Frequentes</h2>
  
  <details class="cp-faq__item">
    <summary>[PERGUNTA 1]</summary>
    <p>[Resposta 2-5 linhas]</p>
  </details>
  
  <details class="cp-faq__item">
    <summary>[PERGUNTA 2]</summary>
    <p>[Resposta 2-5 linhas]</p>
  </details>
  
  <!-- EXATAMENTE 6 perguntas -->
</section>
CSS:

CSS

.cp-faq {
  margin: 40px 0;
}

.cp-faq__item {
  background: white;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  padding: 16px 20px;
  margin-bottom: 12px;
  cursor: pointer;
  transition: all 0.3s;
}

.cp-faq__item:hover {
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

.cp-faq__item summary {
  font-weight: 600;
  color: #1428A0;
  outline: none;
  user-select: none;
}

.cp-faq__item[open] summary {
  color: #0ea5e9;
  margin-bottom: 12px;
}

.cp-faq__item p {
  margin: 0;
  color: #555;
  line-height: 1.6;
}
BLOCO 17: Veredito Final
HTML

<section id="veredito" class="cp-verdict">
  <h2>✅ Veredito Final</h2>
  
  <p>
    [Parágrafo 100-150 palavras, resumindo a proposta e alinhando 
    com a resposta rápida/nota final]
  </p>
  
  <div class="cp-verdict__recommendation">
    <p><strong>Recomendação:</strong> [SIM/DEPENDE/NÃO] — [1 frase clara]</p>
  </div>
</section>
CSS:

CSS

.cp-verdict {
  margin: 40px 0;
}

.cp-verdict__recommendation {
  background: #f0fdf4;
  border-left: 4px solid #22c55e;
  padding: 16px 20px;
  border-radius: 6px;
  margin-top: 20px;
}

.cp-verdict__recommendation p {
  margin: 0;
  font-size: 15px;
  color: #166534;
  line-height: 1.6;
}
BLOCO 18: Escolha Rápida
HTML

<section class="cp-quick-choice">
  <h2>⚡ Escolha Rápida: 3 Cenários</h2>
  
  <div class="cp-quick-choice__grid">
    <div class="cp-quick-choice__item">
      <p style="font-size: 28px; margin: 0 0 8px 0;">🎓</p>
      <p style="font-weight: 700; color: #166534; margin: 0 0 8px 0;">
        [Cenário 1]
      </p>
      <p style="font-size: 14px; color: #555; margin: 0;">
        [Recomendação breve]
      </p>
    </div>
    
    <div class="cp-quick-choice__item">
      <p style="font-size: 28px; margin: 0 0 8px 0;">💼</p>
      <p style="font-weight: 700; color: #1e40af; margin: 0 0 8px 0;">
        [Cenário 2]
      </p>
      <p style="font-size: 14px; color: #555; margin: 0;">
        [Recomendação breve]
      </p>
    </div>
    
    <div class="cp-quick-choice__item">
      <p style="font-size: 28px; margin: 0 0 8px 0;">🔄</p>
      <p style="font-weight: 700; color: #92400e; margin: 0 0 8px 0;">
        [Cenário 3]
      </p>
      <p style="font-size: 14px; color: #555; margin: 0;">
        [Recomendação breve]
      </p>
    </div>
  </div>
</section>
CSS:

CSS

.cp-quick-choice__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 20px;
}

.cp-quick-choice__item {
  background: #f8f9fa;
  border: 1px solid #e2e8f0;
  border-radius: 10px;
  padding: 18px;
  text-align: center;
}

@media (max-width: 768px) {
  .cp-quick-choice__grid {
    grid-template-columns: 1fr;
  }
}
BLOCO 19: CTAs Finais
HTML

<section class="cp-cta-final">
  <h2 id="onde-comprar">🛒 Onde Comprar</h2>
  
  <div class="cp-cta-final__cards">
    <a href="[LINK_AMAZON]" rel="sponsored noopener noreferrer" 
       target="_blank" class="cp-cta-final__card cp-cta-final__card--amazon">
      <div class="cp-cta-final__card-header">🔗 Ver na Amazon</div>
      <p class="cp-cta-final__card-price">R$ [PREÇO]</p>
      <p class="cp-cta-final__card-note">[Parcelado em até 12x]</p>
    </a>
    
    <a href="[LINK_ML]" rel="sponsored noopener noreferrer" 
       target="_blank" class="cp-cta-final__card cp-cta-final__card--mercadolivre">
      <div class="cp-cta-final__card-header">🔗 Ver no Mercado Livre</div>
      <p class="cp-cta-final__card-price">R$ [PREÇO]</p>
      <p class="cp-cta-final__card-note">[Frete grátis/Promoção]</p>
    </a>
    
    <a href="[LINK_OFICIAL]" rel="noopener" 
       target="_blank" class="cp-cta-final__card cp-cta-final__card--official">
      <div class="cp-cta-final__card-header">🔗 Loja Oficial</div>
      <p class="cp-cta-final__card-price">R$ [PREÇO]</p>
      <p class="cp-cta-final__card-note">[Sem comissão/Garantia]</p>
    </a>
  </div>
  
  <p style="text-align: center; font-size: 12px; color: #888; margin-top: 20px;">
    ⚠️ Preços verificados em [DATA] · Sujeitos a alteração
  </p>
</section>
CSS:

CSS

.cp-cta-final__cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 20px;
}

.cp-cta-final__card {
  background: white;
  border: 2px solid #e5e7eb;
  border-radius: 10px;
  padding: 18px;
  text-decoration: none;
  transition: all 0.3s;
  display: block;
}

.cp-cta-final__card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.cp-cta-final__card--amazon {
  border-top-color: #FF9900;
  border-top-width: 3px;
}

.cp-cta-final__card--mercadolivre {
  border-top-color: #3485DB;
  border-top-width: 3px;
}

.cp-cta-final__card--official {
  border-top-color: #22c55e;
  border-top-width: 3px;
}

.cp-cta-final__card-header {
  font-weight: 700;
  font-size: 15px;
  color: #1a1a2e;
  margin-bottom: 8px;
}

.cp-cta-final__card-price {
  margin: 0 0 4px 0;
  font-size: 18px;
  font-weight: 700;
  color: #1428A0;
}

.cp-cta-final__card-note {
  margin: 0;
  font-size: 12px;
  color: #888;
}

@media (max-width: 768px) {
  .cp-cta-final__cards {
    grid-template-columns: 1fr;
  }
}
BLOCO 20: Fontes Consultadas
HTML

<footer id="fontes" class="cp-sources">
  <h2>📚 Fontes Consultadas</h2>
  
  <div class="cp-sources__section">
    <h3>Oficiais</h3>
    <ul>
      <li>
        <a href="[URL]" rel="noopener" target="_blank">
          [Fabricante — Especificações Oficiais]
        </a>
        — acessado em [DD/MM/AAAA]
      </li>
    </ul>
  </div>
  
  <div class="cp-sources__section">
    <h3>Varejo (preços verificados em [DATA])</h3>
    <ul>
      <li>
        <a href="[URL]" rel="noopener" target="_blank">
          Amazon — [Variante]
        </a>
      </li>
      <li>
        <a href="[URL]" rel="noopener" target="_blank">
          Mercado Livre — [Anúncio]
        </a>
      </li>
    </ul>
  </div>
</footer>
CSS:

CSS

.cp-sources {
  background: #f8fafc;
  border-left: 4px solid #1428A0;
  padding: 20px 24px;
  border-radius: 8px;
  margin-top: 40px;
}

.cp-sources h2 {
  margin-top: 0;
}

.cp-sources__section {
  margin-bottom: 20px;
}

.cp-sources__section h3 {
  font-size: 14px;
  text-transform: uppercase;
  color: #64748b;
  margin: 0 0 12px 0;
  letter-spacing: 0.3px;
}

.cp-sources__section ul {
  margin: 0;
  padding-left: 20px;
  line-height: 1.8;
}

.cp-sources__section a {
  color: #1428A0;
  text-decoration: none;
  font-weight: 500;
}

.cp-sources__section a:hover {
  text-decoration: underline;
}
3.3 Checklist de validação REVIEW (46 itens)
Markdown

## ✅ PRÉ-ENTREGA REVIEW — Checklist Obrigatório

### BLOCOS ESTRUTURAIS (20)
[ ] 1. Meta descrição presente (comentário HTML topo)
[ ] 2. Hero Section com gradiente correto da marca
[ ] 3. Imagem principal com Alt Text rico em LSI ([IMAGEM AQUI])
[ ] 4. Metodologia amarela com link para /como-avaliamos/
[ ] 5. Prova social grid 2x2 (2 Amazon + 2 Mercado Livre)
[ ] 6. Índice com 10 âncoras funcionando
[ ] 7. Introdução com keyword em negrito
[ ] 8. Aviso de afiliado vermelho
[ ] 9. CTAs topo (1-2 cards com links válidos)
[ ] 10. Prós/contras grid verde/vermelho

### CONTEÚDO EDITORIAL
[ ] 11. Especificações técnica (máx 8 linhas, todas com fonte)
[ ] 12. Mínimo 3 H2 de análise detalhada
[ ] 13. Comparativo vs 2-3 rivais com preços datados
[ ] 14. Para Quem É com 3+ perfis positivos
[ ] 15. Para Quem NÃO É com alternativas

### NOTAS E CÁLCULO
[ ] 16. Grid 3x2 de notas presente (6 critérios ou N/A)
[ ] 17. Cada nota é múltiplo de 0,5 (8,5 / 9,0 / 8,0 etc)
[ ] 18. Nenhuma nota decimal além de 0,5 (proibido 8,7)
[ ] 19. Nota final calculada e validada
[ ] 20. Selo correto (🏆/⭐/👍/⚖️/⚠️)
[ ] 21. Link para /como-avaliamos/ no bloco de notas

### FAQ E VEREDITO
[ ] 22. Exatamente 6 perguntas em <details>
[ ] 23. Veredito final alinhado com nota
[ ] 24. Escolha rápida com 3 cenários
[ ] 25. CTAs finais com 3 cards (Amazon/ML/Oficial)

### IMAGENS
[ ] 26. [IMAGEM AQUI] marcado em Bloco 3
[ ] 27. [IMAGEM AQUI] marcado em Bloco 13 (se comparativo)
[ ] 28. RELATÓRIO DE IMAGENS presente com prompts DALL-E
[ ] 29. Dimensões especificadas para cada imagem
[ ] 30. Instruções passo-a-passo incluídas

### TRANSPARÊNCIA
[ ] 31. Datas verificadas em TODAS as comparações
[ ] 32. Links com rel="sponsored nofollow" (afiliados)
[ ] 33. Links oficiais sem rel="sponsored" (dofollow)
[ ] 34. Aviso final: "Preços verificados em [DATA]"
[ ] 35. Fontes consultadas com URLs diretas

### SEO
[ ] 36. Keyword exata no 1º parágrafo (negrito)
[ ] 37. Meta descrição 155-160 caracteres
[ ] 38. Título SEO ≤ 60 caracteres, sem "teste" falso
[ ] 39. Alt text imagem contém keyword
[ ] 40. Nenhuma frase "testamos", "usamos", "comprovamos"

### LINKS E TÉCNICO
[ ] 41. Todos os links funcionam (sem 404)
[ ] 42. Links afiliados apontam para página correta
[ ] 43. Nenhuma classe CSS nova (apenas cp-*)
[ ] 44. Nenhum bloco reordenado
[ ] 45. Imagens carregam sem erro
[ ] 46. HTML válido (sem tags abertas)

❌ SE QUALQUER ITEM FALHAR: NÃO ENTREGAR
   Corrigir + Re-validar checklist
4. TEMPLATE-LISTA-LOCKED
4.1 Ordem obrigatória dos 15 blocos
Meta Descrição SEO
Hero Section (gradient neutro ou cor principal)
Imagem Principal
Metodologia
Introdução
Aviso Afiliado
Índice
Card Ranking #1 (produto + nota + prova social 2x2)
Card Ranking #2
Card Ranking #3 (ou mais, conforme "Top X")
Tabela Comparativa (todos os produtos da lista)
FAQ
Para Quem É
CTAs Finais
Fontes Consultadas
4.2 Estrutura do Card Ranking (repetido para cada produto)
HTML

<section class="cp-ranking-item" id="produto-1">
  <div class="cp-ranking-item__header">
    <span class="cp-ranking-item__position">🥇 1º Lugar</span>
    <h3 class="cp-ranking-item__title">[PRODUTO]</h3>
    <span class="cp-ranking-item__rating">
      [X.X]/10 · [SELO]
    </span>
  </div>
  
  <p class="cp-ranking-item__summary">
    [Resumo 2-3 linhas por que é o melhor]
  </p>
  
  <!-- PROVA SOCIAL 2x2 -->
  <div class="cp-ranking-item__social">
    <div class="cp-review-card cp-review-card--amazon">
      <strong>Amazon</strong><br>
      ⭐ [X.X]/5 · [N] avaliações<br>
      <em>"[Transcrição curta]"</em>
    </div>
    <div class="cp-review-card cp-review-card--mercadolivre">
      <strong>Mercado Livre</strong><br>
      ⭐ [X.X]/5 · [N] opiniões<br>
      <em>"[Transcrição curta]"</em>
    </div>
  </div>
  
  <!-- SPECS RESUMIDAS -->
  <div class="cp-ranking-item__specs">
    <h4>Especificações principais</h4>
    <ul>
      <li>[Spec 1]</li>
      <li>[Spec 2]</li>
      <li>[Spec 3]</li>
      <li>[Spec 4]</li>
    </ul>
  </div>
  
  <!-- NOTAS PARCIAIS -->
  <div class="cp-ranking-item__ratings">
    <div>[Critério 1] · [X.X]/10</div>
    <div>[Critério 2] · [X.X]/10</div>
    <div>[Critério 3] · [X.X]/10</div>
  </div>
  
  <!-- CTA -->
  <a href="[LINK]" rel="sponsored noopener noreferrer" 
     target="_blank" class="cp-ranking-item__cta">
    Ver preço na Amazon
  </a>
</section>
4.3 Checklist LISTA (30+ itens)
Markdown

[ ] Meta descrição presente
[ ] Hero com título "Top X [Categoria] 2026"
[ ] Introdução clara: "selecionamos X produtos"
[ ] Metodologia link para /como-avaliamos/
[ ] Cada card ranking completo (título + nota + prova social)
[ ] Prova social 2x2 em cada card
[ ] Specs resumidas (4-5 itens principais)
[ ] Notas parciais por produto
[ ] Tabela comparativa todos vs todos
[ ] FAQ 6+ perguntas
[ ] Para Quem É section
[ ] CTAs finais com 3-5 opções
[ ] Datas verificadas explícitas
[ ] Links funcionam
[ ] Sem "testamos"
[ ] RELATÓRIO DE IMAGENS com prompts
5. TEMPLATE-VS-LOCKED
5.1 Ordem obrigatória dos 18 blocos
Meta Descrição
Hero ("X ou Y: qual comprar")
Imagem Principal (produtos lado a lado)
Metodologia
Prova Social (2x2 por produto: 2 Amazon + 2 ML)
Índice
Introdução
Aviso Afiliado
Botões Topo (ambos produtos)
Resposta Rápida (3 cards: adequado/depende/espera)
Tabela Comparativa (lado a lado com winner marks)
Análise Produto A (H2 específico)
Análise Produto B (H2 específico)
Análise Produto C (se houver)
Compre se / Não Compre se
Cenários Rápidos (3 escolhas)
FAQ
CTAs Finais
5.2 Checklist VS (30+ itens)
Markdown

[ ] Meta descrição "X ou Y: qual comprar"
[ ] Hero com título "X vs Y: qual comprar 2026"
[ ] Prova social 2x2 PARA CADA PRODUTO
[ ] Tabela comparativa com winner marks
[ ] Análise individual de cada produto (H2)
[ ] Resposta rápida: 3 cards
[ ] Cenários de compra (3)
[ ] Para quem cada um é bom
[ ] CTAs topo + final
[ ] Datas de preço verificadas
[ ] Imagem comparativo bloco 13 [IMAGEM AQUI]
[ ] RELATÓRIO DE IMAGENS com prompts
[ ] Todos os links funcionam
6. PROTOCOLO-AGENT (VERSÃO CORRIGIDA)
6.1 Fluxo completo (pesquisa → cálculo → renderização)
O Agent NÃO espera que você forneça as notas.

Agent executa tudo automaticamente:

text

ENTRADA (briefing mínimo):
  Produto
  Categoria
  Links Amazon/ML
  Concorrentes
  ↓
FASE 1: PESQUISA
  [ ] Extrair specs oficiais
  [ ] Coletar avaliações Amazon/ML
  [ ] Buscar reviews especializados
  [ ] Copiar comentários reais (transcrição fiel)
  ↓
FASE 2: ANÁLISE + CÁLCULO
  [ ] Analisar Custo-benefício
  [ ] Analisar Satisfação verificada
  [ ] Analisar Ficha técnica
  [ ] Analisar Recursos e usabilidade
  [ ] Analisar Consenso técnico
  [ ] Analisar Confiança e suporte
  [ ] Calcular nota final (fórmula v2.0)
  [ ] Definir selo
  ↓
FASE 3: RENDERIZAÇÃO
  [ ] Carregar template correto (REVIEW/LISTA/VS)
  [ ] Preencher 20 blocos (ou 15/18)
  [ ] Grid 3x2 com 6 notas calculadas
  [ ] Prova social 2x2 com comentários reais
  [ ] Todas análises já integradas no HTML
  [ ] Imagens como [IMAGEM AQUI] (placeholders)
  ↓
FASE 4: RELATÓRIO DE IMAGENS
  [ ] Gerar prompts DALL-E para cada imagem
  [ ] Listar dimensões, locais, instruções
  ↓
SAÍDA: 
  - HTML final completo (pronto para WordPress)
  - RELATÓRIO DE IMAGENS (2-3 prompts prontos)
6.2 Briefing MÍNIMO que você fornece
Markdown

Próximo artigo: [REVIEW / LISTA / VS]

PRODUTO: [Nome exato]
CATEGORIA: [Smartphone / Notebook / Fone / TV / etc]

LINKS:
- Amazon: [URL específica do produto]
- Mercado Livre: [URL específica do produto]

CONCORRENTES: [Produto A, Produto B, Produto C]
É só isso. Nada de notas, nada de análises, nada de imagens.

6.3 O que o Agent pesquisa automaticamente
Para Custo-benefício (30%)
Agent busca:

Preço na data de hoje (Amazon + ML)
Specs do produto (ficha técnica oficial)
Preço + specs dos 2-3 concorrentes na mesma data
Pergunta: "este produto entrega mais por menos?"
Para Satisfação verificada (25%)
Agent extrai:

Nota média Amazon (com número de avaliações)
Nota média Mercado Livre (com número de opiniões)
2 comentários Amazon (transcrição fiel, nome, data, úteis)
2 comentários Mercado Livre (transcrição fiel, nome, data)
Padrão das avaliações (há defeitos recorrentes?)
Pergunta: "compradores aprovam? Há problemas?"
Para Ficha técnica (20%)
Agent consulta:

Site oficial do fabricante
Manual em PDF (se disponível)
Especificações contra o padrão da categoria
Pergunta: "estas specs são boas para a faixa de preço?"
Para Recursos e usabilidade (10%)
Agent verifica:

App oficial existe? Qual versão?
Quantas portas? Quais tipos?
Sistema operacional qual versão?
Recursos declarados (ANC, multiponto, etc)
Relatos de compradores verificados sobre operação
Pergunta: "o que o produto DE FATO faz no dia a dia?"
Para Consenso técnico (10%)
Agent busca:

Reviews de canais especializados (YouTube tech, sites tech)
Há convergência? Todos apontam os mesmos pontos?
Há discordância? Detalhe.
Pergunta: "especialistas independentes concordam?"
Para Confiança e suporte (5%)
Agent verifica:

Garantia Brasil quanto tempo?
Assistência técnica funciona?
App recebe atualizações regularmente?
Histórico da marca (consolidada? abandona produtos?)
Pergunta: "se der ruim, tenho suporte?"
6.4 Cálculo das 6 notas (detalhado)
Agent calcula cada nota de 0 a 10 baseado em:

text

Custo-benefício (30%):
  Escala:
    9.5-10  → Melhor preço e specs da categoria
    9.0-9.4 → Muito bom custo-benefício
    8.0-8.9 → Bom, mas existe alternativa barata
    7.0-7.9 → Aceitável
    < 7.0  → Caro demais para o que oferece

Satisfação verificada (25%):
  Critério:
    9.5-10  → 4.8+/5 com 1000+ avaliações convergentes
    9.0-9.4 → 4.5-4.7/5 com volume alto
    8.0-8.9 → 4.0-4.4/5, defeitos menores
    7.0-7.9 → 3.8-3.9/5, problemas recorrentes
    < 7.0  → < 3.8/5 ou defeitos graves

Ficha técnica (20%):
  Critério:
    9.5-10  → Specs excedem padrão da categoria
    9.0-9.4 → Specs muito boas para a faixa
    8.0-8.9 → Specs boas, alguns limitantes
    7.0-7.9 → Specs aceitáveis, alguns pontos fracos
    < 7.0  → Specs limitadas para o preço

Recursos e usabilidade (10%):
  Critério:
    9.5-10  → App rico + muitos controles + relatos muito positivos
    9.0-9.4 → App bom + controles confiáveis + relatos positivos
    8.0-8.9 → App funcional + alguns limites + relatos neutros
    7.0-7.9 → App básico + poucas opções + relatos mistos
    < 7.0  → App ruim ou ausente + relatos negativos

Consenso técnico (10%):
  Critério:
    9.5-10  → Todos especialistas concordam, referência
    9.0-9.4 → Maioria concorda, poucos pontos de discordância
    8.0-8.9 → Há consenso em geral, algumas ressalvas
    7.0-7.9 → Opiniões divididas, não há consenso claro
    < 7.0  → Discordância forte ou reviews muito negativos

Confiança e suporte (5%):
  Critério:
    9.5-10  → Garantia 2+ anos, assistência excelente, marca premium
    9.0-9.4 → Garantia 1-2 anos, assistência boa, marca confiável
    8.0-8.9 → Garantia 1 ano, assistência funciona, marca conhecida
    7.0-7.9 → Garantia curta ou assistência lenta, marca menos conhecida
    < 7.0  → Sem garantia clara ou assistência ruim
6.5 Cálculo da nota final (fórmula)
Agent executa:

text

Nota Final = (N1 × 0.30) + (N2 × 0.25) + (N3 × 0.20) 
           + (N4 × 0.10) + (N5 × 0.10) + (N6 × 0.05)

Exemplo (Samsung S25):
  = (9.5 × 0.30) + (9.0 × 0.25) + (9.0 × 0.20)
    + (9.0 × 0.10) + (8.5 × 0.10) + (8.0 × 0.05)
  = 2.850 + 2.250 + 1.800 + 0.900 + 0.850 + 0.400
  = 9.050

Arredondar: 9.050 → 9.0/10 (múltiplo de 0,5)

Selo: 9.0 ≥ 9.0 → 🏆 Melhor da categoria
6.6 Regra N/A (critério não se aplica)
Se um critério não se aplica (ex: fone não tem câmera):

text

1. Marcar como N/A
2. Remover o peso desse critério
3. Redistribuir proporcionalmente entre os 5 restantes

Exemplo: Consenso técnico N/A (fone muito nicho)
  Peso original: 10%
  Soma restante: 90%
  
  Novo peso Custo: 30 ÷ 0.90 = 33,3%
  Novo peso Satisfação: 25 ÷ 0.90 = 27,8%
  Novo peso Ficha: 20 ÷ 0.90 = 22,2%
  Novo peso Recursos: 10 ÷ 0.90 = 11,1%
  Novo peso Confiança: 5 ÷ 0.90 = 5,6%

Declarar no texto: "Consenso técnico foi marcado N/A porque..."
6.7 Renderização final (REVIEW)
Agent carrega TEMPLATE-REVIEW-LOCKED e preenche:

HTML

BLOCO 1:  Meta descrição
BLOCO 2:  Hero (com cor da marca)
BLOCO 3:  Imagem principal [IMAGEM AQUI]
BLOCO 4:  Metodologia (link para /como-avaliamos/)
BLOCO 5:  Prova social grid 2x2 (2 Amazon + 2 ML)
BLOCO 6:  Índice
BLOCO 7:  Introdução (keyword no 1º parágrafo)
BLOCO 8:  Aviso afiliado
BLOCO 9:  CTAs topo
BLOCO 10: Prós/contras
BLOCO 11: Specs (máx 8 linhas)
BLOCO 12: Análise detalhada (≥3 H2)
         [Aqui vão as análises calculadas, 
          integradas ao texto — não em boxes separados]
BLOCO 13: Comparativo vs concorrentes [IMAGEM AQUI]
BLOCO 14: Para quem é/não é
BLOCO 15: Grid 3x2 com 6 notas calculadas
BLOCO 16: FAQ (exatamente 6)
BLOCO 17: Veredito (alinhado com nota)
BLOCO 18: Escolha rápida (3 cenários)
BLOCO 19: CTAs finais
BLOCO 20: Fontes consultadas
6.8 Saída (o que você recebe)
Agent entrega:

text

✅ HTML completo (pronto para copiar/colar no WordPress)
✅ 20 blocos LOCKED presentes
✅ 6 notas calculadas e integradas
✅ Prova social 2x2 real (comentários copiados de Amazon/ML)
✅ Análises já escritas e integradas ao texto
✅ Imagens como [IMAGEM AQUI] (placeholders)
✅ RELATÓRIO DE IMAGENS (prompts + instruções)
✅ Checklist 40+ itens validado
✅ Nota final: [X.X]/10
✅ Selo: [🏆/⭐/👍/⚖️/⚠️]
Você apenas:

Gera imagens (DALL-E/Midjourney)
Faz upload no WordPress
Substitui URLs no HTML
Copia/cola no WordPress
6.9 Exemplo de prompt COMPLETO
Markdown

Próximo artigo: REVIEW

PRODUTO: Apple iPhone 16 Pro
CATEGORIA: Smartphone

LINKS:
- Amazon: https://www.amazon.com.br/Apple-iPhone-16-Pro-256GB/dp/B0DFH8...
- Mercado Livre: https://produto.mercadolivre.com.br/MLB-...

CONCORRENTES: Samsung Galaxy S25, Pixel 9 Pro

---

Pesquise, calcule as 6 notas conforme régua v2.0,
gere HTML com [IMAGEM AQUI] como placeholders,
e entregue RELATÓRIO DE IMAGENS com prompts DALL-E.
6.10 Validação automática pré-entrega
Agent DEVE rodar antes de entregar:

text

CHECKLIST 46 ITENS:

BLOCOS ESTRUTURAIS (20)
[ ] 1 Meta descrição
[ ] 2 Hero Section
[ ] 3 Imagem principal [IMAGEM AQUI]
[ ] 4 Metodologia + link
[ ] 5 Prova social 2x2 (2+2)
[ ] 6 Índice
[ ] 7 Introdução
[ ] 8 Aviso afiliado
[ ] 9 CTAs topo
[ ] 10 Prós/contras
[ ] 11 Specs (max 8)
[ ] 12 Análise ≥3 H2
[ ] 13 Comparativo [IMAGEM AQUI]
[ ] 14 Para quem é
[ ] 15 Grid 3x2 notas
[ ] 16 FAQ (exactly 6)
[ ] 17 Veredito
[ ] 18 Escolha rápida
[ ] 19 CTAs finais
[ ] 20 Fontes

NOTAS (6)
[ ] 21 Nota 1 é múltiplo 0,5
[ ] 22 Nota 2 é múltiplo 0,5
[ ] 23 Nota 3 é múltiplo 0,5
[ ] 24 Nota 4 é múltiplo 0,5
[ ] 25 Nota 5 é múltiplo 0,5
[ ] 26 Nota 6 é múltiplo 0,5
[ ] 27 Nota final bate fórmula
[ ] 28 Selo correto para faixa

IMAGENS
[ ] 29 [IMAGEM AQUI] marcado em Bloco 3
[ ] 30 [IMAGEM AQUI] marcado em Bloco 13 (se VS)
[ ] 31 RELATÓRIO DE IMAGENS presente
[ ] 32 Prompts DALL-E completos e claros
[ ] 33 Dimensões especificadas para cada imagem
[ ] 34 Instruções passo-a-passo incluídas

TRANSPARÊNCIA (8)
[ ] 35 Datas verificadas explícitas
[ ] 36 Links Amazon têm rel="sponsored nofollow"
[ ] 37 Links ML têm rel="sponsored nofollow"
[ ] 38 Links oficiais SEM rel="sponsored"
[ ] 39 Nenhuma frase "testamos"/"usamos"
[ ] 40 Alt text contém keyword
[ ] 41 Meta description 155-160 chars
[ ] 42 Título SEO ≤ 60 chars

TÉCNICO (4)
[ ] 43 Nenhuma classe CSS nova
[ ] 44 Todos links funcionam
[ ] 45 HTML válido (sem tags abertas)
[ ] 46 Placeholders [IMAGEM AQUI] presentes nos blocos corretos

SE QUALQUER ITEM FALHAR:
  ❌ NÃO ENTREGAR
  ⚠️ Avisar qual item falta
  🔧 Corrigir e rodar checklist novamente
6.11 Relatório de Imagens (NOVO)
Agent DEVE entregar junto com HTML um relatório estruturado com as imagens necessárias.

O que é o Relatório
Documento separado contendo:

Qual imagem é necessária
Onde vai no HTML (bloco número)
Dimensões exatas
Prompt DALL-E/Midjourney pronto para copiar
Instruções passo-a-passo (gerar → comprimir → upload → substituir)
Tipos de imagens por artigo
REVIEW: 2 imagens

text

1. THUMBNAIL (Featured Image do WordPress)
2. HERO (Bloco 3 do HTML)
VS/COMPARATIVO: 3 imagens

text

1. THUMBNAIL (Featured Image)
2. HERO (Bloco 3)
3. COMPARATIVO (Bloco 13 - lado a lado)
LISTA/GUIA: 2 imagens

text

1. THUMBNAIL (Featured Image)
2. HERO (Bloco 3)
Estrutura do Relatório (EXEMPLO: Samsung S25)
Markdown

# 📊 RELATÓRIO DE IMAGENS
## Samsung Galaxy S25 5G - REVIEW

Gerado em: [DATA/HORA]
Tipo de artigo: REVIEW
Imagens necessárias: 2

---

## 1️⃣ THUMBNAIL (Featured Image - WordPress Media)

**Local:** 
- WordPress Media Library
- Defina como "Featured Image" do post

**Dimensões:** 
- 1200 x 630 pixels (16:9 aspect ratio)

**Tipo:** 
- Imagem de capa/destaque do artigo

**Descrição do conteúdo:**
- Produto (Samsung Galaxy S25 5G em Azul Marinho)
- Texto: "Samsung Galaxy S25 5G" + "8.5/10 ⭐ Recomendado"
- Logo Curadoria Prime (canto inferior direito)
- Background: Gradiente azul Samsung (#1428A0)

---

### Prompt para DALL-E / Midjourney:
Create a premium product thumbnail for a tech review website:

DIMENSIONS: 1200x630px (16:9 landscape)
PRODUCT: Samsung Galaxy S25 5G smartphone in Midnight Blue
STYLE: Modern, professional, premium tech aesthetic

LAYOUT:

Background: Gradient (Dark Blue #1428A0 to Light Blue)
Product image: Centered, 45° angle view, well-lit
Text overlay (top left): Bold white text "Samsung Galaxy S25 5G"
Rating overlay (center): Large yellow star ⭐ + "8.5/10" + "Recomendado"
Branding (bottom right): Small white text "Curadoria Prime 🎯"
STYLE REFERENCE:

Similar to Apple.com product pages
Premium, clean, minimalist
High-quality lighting
Professional feel
High contrast for readability
FORMAT: WEBP or JPG
QUALITY: High (suitable for web, < 100KB when compressed)

text


---

### Instruções passo-a-passo:

**Passo 1: Gerar a imagem**
Acesse chat.openai.com (DALL-E)
OU discord.com/channels/[Midjourney]

Cole o prompt acima (completo)

DALL-E: Gere 4 variações, escolha a melhor
Midjourney: Digite /imagine [prompt]

Selecione a versão mais próxima (cores, composição)

Download em alta qualidade (PNG ou JPG)

text


**Passo 2: Comprimir a imagem**
Acesse TinyPNG.com

Faça upload do arquivo

Clique "Compress"

Download em WEBP (melhor compressão)

Resultado esperado: 80-100KB

text


**Passo 3: Upload no WordPress**
WordPress Dashboard → Media → Add New

Faça upload do arquivo WEBP

Preencha:

Alt Text: "Samsung Galaxy S25 5G review thumbnail 8.5/10"
Description: "Thumbnail for Samsung Galaxy S25 5G review"
Clique "Upload"

Copie a URL: https://curadoriaprime.com/wp-content/uploads/[ano/mês/arquivo].webp

text


**Passo 4: Definir como Featured Image**
Na página/post do artigo

Lado direito (WordPress Editor)

Clique em "Featured Image"

Selecione o arquivo que acabou de fazer upload

Salve o post (RASCUNHO)

text


**URL final esperada:**
https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-thumbnail.webp

text


---

## 2️⃣ HERO (Imagem dentro do HTML - Bloco 3)

**Local:** 
- HTML Bloco 3 (logo após Metodologia)
- Tag: `<img src="[IMAGEM AQUI]">`

**Dimensões:** 
- 970 x 510 pixels (16:9 aspect ratio)

**Tipo:** 
- Produto frontal, estúdio, sem texto

**Descrição do conteúdo:**
- Samsung Galaxy S25 5G em Azul Marinho
- Ângulo: 45° frontal
- Iluminação premium/estúdio
- Sem sobreposição de texto
- Background: Branco suave a azul claro

---

### Prompt para DALL-E / Midjourney:
Create a premium product showcase image for website article:

DIMENSIONS: 970x510px (16:9 landscape)
PRODUCT: Samsung Galaxy S25 5G in Midnight Blue

POSITIONING:

Angle: 45° frontal view (showing front and side)
Centered in frame
Well-lit, premium studio lighting
BACKGROUND:

Soft gradient: White to Light Blue (#E8F4FF)
Clean, minimalist, no clutter
Subtle shadow under product
STYLE:

Professional product photography
Similar to Apple.com, Samsung.com product pages
Premium, high-end tech feel
No text overlay
Sharp, detailed, high quality
DETAILS:

Show both front screen and side profile
Emphasize design and build quality
Highlight blue color accurately
Professional lighting (no harsh shadows)
FORMAT: WEBP or JPG
QUALITY: High (suitable for web, < 80KB when compressed)

text


---

### Instruções passo-a-passo:

**Passo 1: Gerar**
Acesse DALL-E ou Midjourney

Cole o prompt acima

Gere 4 variações

Escolha a que melhor mostra o produto em ângulo

text


**Passo 2: Comprimir**
TinyPNG.com

Upload → Compress → Download WEBP

Resultado: < 80KB

text


**Passo 3: Upload no WordPress Media**
WordPress → Media → Add New

Upload do arquivo WEBP

Alt Text: "Samsung Galaxy S25 5G smartphone premium design 2026"

Description: "Hero image for Samsung Galaxy S25 5G review"

Copy URL: https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-hero.webp

text


**Passo 4: Substituir no HTML**
Encontre no HTML:

<img src="[IMAGEM AQUI]" alt="..." class="cp-hero__img">
Substitua por:

<img src="https://curadoriaprime.com/wp-content/uploads/2026/08/samsung-s25-hero.webp" alt="Samsung Galaxy S25 5G smartphone premium design 2026" class="cp-hero__img">

text


---

## ✅ CHECKLIST FINAL DE IMAGENS

[ ] Thumbnail gerado e comprimido (< 100KB)
[ ] Thumbnail feito upload no WP Media
[ ] Thumbnail definido como Featured Image
[ ] Hero gerado e comprimido (< 80KB)
[ ] Hero feito upload no WP Media
[ ] Hero URL copiada e colada no HTML (Bloco 3)
[ ] Ambas imagens testadas (links funcionam)
[ ] Alt text preenchido para ambas
[ ] Prompts DALL-E salvos para referência futura

---

## 📌 RESUMO VISUAL

| # | Imagem | Local | Dimensões | Onde Upload | Ação |
|---|--------|-------|-----------|-------------|------|
| 1 | Thumbnail | Featured Image WP | 1200x630 | Media Library | Definir como Featured |
| 2 | Hero | Bloco 3 (HTML) | 970x510 | Media Library | Substituir [IMAGEM AQUI] |

---

**Gerado por:** Curadoria Prime Agent
**Data:** [ATUAL]
**Pronto para:** DALL-E / Midjourney
Integração com o HTML
Agent coloca no HTML:

HTML

<!-- BLOCO 3: IMAGEM PRINCIPAL -->
<figure class="cp-featured-image">
  <img 
    src="[IMAGEM AQUI]" 
    alt="Samsung Galaxy S25 5G smartphone premium design 2026" 
    class="cp-featured-image__img"
    loading="lazy"
  >
  <figcaption class="cp-featured-image__caption">
    Samsung Galaxy S25 5G — Design premium em Azul Marinho com molduras ultrafinas e câmera tripla
  </figcaption>
</figure>
Você substitui [IMAGEM AQUI] pela URL do WP.

7. VALIDADOR AUTOMÁTICO
7.1 Checklist de blocos (pré-entrega obrigatória)
Antes de qualquer artigo sair, o Agent executa:

text

REVIEW (20 blocos)
[ ] 1 ✅ Meta SEO
[ ] 2 ✅ Hero
[ ] 3 ✅ Imagem
[ ] 4 ✅ Metodologia
[ ] 5 ✅ Prova Social (2x2)
[ ] 6 ✅ Índice
[ ] 7 ✅ Introdução
[ ] 8 ✅ Aviso Afiliado
[ ] 9 ✅ CTAs Topo
[ ] 10 ✅ Prós/Contras
[ ] 11 ✅ Specs
[ ] 12 ✅ Análise (≥3 H2)
[ ] 13 ✅ Comparativo
[ ] 14 ✅ Para Quem É
[ ] 15 ✅ Notas 3x2 (grid com 6 critérios ou N/A)
[ ] 16 ✅ FAQ (exatamente 6)
[ ] 17 ✅ Veredito
[ ] 18 ✅ Escolha Rápida (3 cenários)
[ ] 19 ✅ CTAs Finais
[ ] 20 ✅ Fontes

SE QUALQUER UM FALHAR → ❌ NÃO ENTREGAR
Avisar qual bloco falta e por quê.
7.2 Validação de notas
text

Para cada nota no grid:
  ✅ É múltiplo de 0,5? (8,5 / 9,0 / 7,5 / 6,0)
  ❌ Rejeita: 8,7 / 8,3 / 7,1 / 6,6

Para a nota final:
  ✅ Bate o cálculo da fórmula?
  ❌ Se não bater: avisar diferença e rejeitar

Para o selo:
  ✅ Corresponde à faixa de nota?
  ❌ Se 8,5 mas selo é ⚠️ → erro
7.3 Validação de transparência
text

✅ Todas as datas em DD/MM/AAAA?
✅ Links afiliados têm rel="sponsored nofollow"?
✅ Links oficiais NÃO têm rel="sponsored"?
✅ Nenhuma frase "testamos"/"comprovamos"?
✅ Alt text contém keyword?
✅ Meta descrição 155-160 caracteres?
7.4 Validação técnica
text

✅ Nenhuma classe CSS nova (apenas cp-*)?
✅ Todos os links funcionam (sem 404)?
✅ Imagens carregam?
✅ Nenhum bloco removido?
✅ Nenhum bloco reordenado?
✅ HTML válido (sem tags abertas)?
