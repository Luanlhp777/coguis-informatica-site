# 🍄 Design System — Coguis Informática

> Documento oficial de identidade visual, componentes e padrões front-end da Coguis Informática.

---

## Objetivo

O Design System da Coguis Informática existe para manter consistência visual, técnica e estrutural em todos os projetos da empresa.

Ele deve servir como base para:

- site institucional;
- Blog da Coguis;
- landing pages;
- sites de clientes;
- materiais futuros da Coguis UI.

---

## Princípios

### 1. Consistência

Toda interface deve parecer parte do mesmo ecossistema visual.

### 2. Clareza

A experiência deve ser simples, objetiva e fácil de entender.

### 3. Reutilização

Componentes devem ser reaproveitados sempre que possível.

### 4. Escalabilidade

O projeto deve crescer sem virar bagunça.

### 5. Humanização

A Coguis deve transmitir tecnologia com proximidade, confiança e linguagem acessível.

---

## Identidade Visual

### Cores principais

```css
--color-bg: #040309;
--color-bg-soft: #0a0712;
--color-surface: rgba(12, 8, 21, 0.88);
--color-surface-strong: rgba(16, 11, 29, 0.96);
--color-border: rgba(186, 132, 255, 0.2);
--color-border-strong: rgba(215, 180, 255, 0.42);
--color-text: #fbf8ff;
--color-text-soft: #cbbfe3;
--color-text-muted: #9889b7;
--color-brand: #a855f7;
--color-brand-strong: #c76fff;
--color-brand-deep: #7c3aed;
--color-white: #ffffff;
```

---

## Tipografia

### Fonte de destaque

```css
--font-display: "Space Grotesk", "Trebuchet MS", sans-serif;
```

Usada em:

- títulos principais;
- títulos de seção;
- títulos de cards;
- elementos de destaque.

### Fonte de texto

```css
--font-body: "Manrope", "Segoe UI", sans-serif;
```

Usada em:

- parágrafos;
- listas;
- descrições;
- links;
- textos auxiliares.

---

## Espaçamentos

```css
--space-2xs: 0.375rem;
--space-xs: 0.75rem;
--space-sm: 1rem;
--space-md: 1.5rem;
--space-lg: 2rem;
--space-xl: 3rem;
--space-2xl: 4.5rem;
--space-3xl: 6rem;
```

---

## Radius

```css
--radius-sm: 0.875rem;
--radius-md: 1.25rem;
--radius-lg: 1.75rem;
--radius-xl: 2.5rem;
--radius-pill: 999px;
```

---

## Sombras

```css
--shadow-sm: 0 12px 30px rgba(6, 3, 14, 0.24);
--shadow-md: 0 24px 70px rgba(6, 3, 14, 0.5);
--shadow-glow: 0 0 0 1px rgba(199, 111, 255, 0.1), 0 24px 60px rgba(168, 85, 247, 0.16);
```

---

## Componentes

### Button

Classe base:

```html
<a class="button button--primary" href="#">Solicitar atendimento</a>
```

Variações atuais:

```css
.button
.button--primary
.button--secondary
```

Responsabilidade:

- criar CTAs;
- padronizar links importantes;
- manter consistência entre páginas.

---

### Image Card

Classe base:

```html
<article class="image-card">
  ...
</article>
```

Usado em:

- Hero do Blog;
- Categorias;
- Artigo em destaque;
- Últimos artigos.

Responsabilidade:

- imagem de fundo;
- overlay;
- conteúdo sobreposto;
- hover com leve zoom;
- borda e radius padronizados.

---

### Tags

Exemplo:

```html
<div class="blog-intro__tags">
  <span>💻 Manutenção</span>
</div>
```

Uso:

- categorias;
- temas;
- filtros;
- tópicos de conteúdo.

---

## Padrão de CSS

### Arquivos globais

```text
css/
├── style.css
├── blog.css
├── components/
└── blog/
```

### Componentes globais

```text
css/components/
├── button.css
├── cards.css
├── badges.css
├── tags.css
├── social.css
├── container.css
└── titles.css
```

---

## Regra de manutenção

Antes de criar um novo CSS, verificar se já existe:

1. componente global;
2. componente específico da página;
3. classe utilitária;
4. token no `:root`.

Só criar uma nova classe se realmente for necessário.

---

## Filosofia Coguis UI

A Coguis UI deve ser uma base reutilizável para sites, blogs, landing pages e projetos digitais da Coguis Informática.

Cada componente deve ser:

- claro;
- reutilizável;
- documentado;
- responsivo;
- fácil de manter.

---

## Ordem dos Imports

Todo projeto da Coguis deve seguir a seguinte ordem:

1. Base
2. Components
3. Layout
4. Pages

Os componentes nunca devem ser importados após as páginas.

Isso garante que todas as páginas utilizem a mesma base visual e evita duplicação de CSS.

---

## Card

Classe base

```html
<div class="card">
```

Responsabilidade

- borda

- radius

- sombra

- background

- overflow

Variações

```
.card

.card--interactive

.card--image

.card--glass
```

Regras

O componente não define:

- largura

- altura

- grid

- display

Essas propriedades pertencem à implementação da página.

---

## Histórico

### v0.1.0

- Início da documentação do Design System.
- Definição dos tokens principais.
- Registro dos primeiros componentes.
- Criação da base para a Coguis UI.