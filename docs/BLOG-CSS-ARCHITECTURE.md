# 🍄 Arquitetura CSS — Blog da Coguis Informática

> Documento oficial da arquitetura CSS do Blog da Coguis Informática.

---

# Objetivo

Este documento descreve toda a organização do CSS utilizada no Blog da Coguis Informática.

Seu objetivo é garantir padronização, facilitar manutenção, permitir escalabilidade e servir como documentação técnica para futuros desenvolvedores e projetos da empresa.

---

# Estrutura de Diretórios

```text
css/
├── blog.css
└── blog/
    ├── blog-base.css
    ├── blog-components.css
    ├── blog-hero.css
    ├── blog-intro.css
    ├── blog-categories.css
    ├── blog-featured.css
    ├── blog-latest.css
    ├── blog-study.css
    ├── blog-cta.css
    └── blog-responsive.css
```

---

# Arquivo Principal

O arquivo `blog.css` deve conter apenas as importações dos módulos do Blog.

```css
@import url("./blog/blog-base.css");
@import url("./blog/blog-components.css");
@import url("./blog/blog-hero.css");
@import url("./blog/blog-intro.css");
@import url("./blog/blog-categories.css");
@import url("./blog/blog-featured.css");
@import url("./blog/blog-latest.css");
@import url("./blog/blog-study.css");
@import url("./blog/blog-cta.css");
@import url("./blog/blog-responsive.css");
```

O arquivo principal **não deve conter regras CSS**, apenas as importações dos módulos.

---

# Organização dos Arquivos

## blog-base.css

Responsável pelos estilos globais do Blog.

Exemplos:

- Espaçamento das seções
- Estilos compartilhados
- Classes base
- Categorias
- Elementos comuns

---

## blog-components.css

Contém componentes reutilizáveis.

Atualmente:

- image-card

Futuramente poderá conter:

- badges
- timeline
- gallery
- author-card
- faq-card
- newsletter-card

---

## blog-hero.css

Responsável exclusivamente pela Hero do Blog.

Contém:

- imagem principal
- overlay
- posicionamento
- conteúdo
- CTA

---

## blog-intro.css

Responsável pela seção de boas-vindas.

Contém:

- apresentação do Blog
- tags
- colunas
- introdução

---

## blog-categories.css

Responsável pelos cards de categorias.

Contém:

- layout dos cards
- imagem
- texto
- hover

---

## blog-featured.css

Responsável pelo artigo em destaque.

---

## blog-latest.css

Responsável pelos últimos artigos.

---

## blog-study.css

Responsável pela integração com o projeto Meu Site de Estudos.

---

## blog-cta.css

Responsável pela chamada final para contato.

---

## blog-responsive.css

Centraliza toda a responsividade do Blog.

Nenhum outro arquivo deve possuir media queries, salvo exceções justificadas.

---

# Componentes

## image-card

### Objetivo

Criar um componente reutilizável para qualquer card baseado em imagem.

### Responsabilidades

- posição relativa
- overflow
- border-radius
- imagem de fundo
- overlay
- hover
- animação

### Utilizado em

- Hero
- Categorias
- Artigo em destaque
- Últimos artigos

### Exemplo

```html
<article class="post-card image-card">
```

---

# Convenções

## CSS Modular

Cada arquivo deve possuir responsabilidade única.

Exemplo:

- Hero → hero.css
- Categorias → categories.css

Nunca misturar componentes diferentes.

---

## Componentes

Sempre reutilizar componentes antes de criar novas regras.

---

## Responsividade

Toda responsividade deverá ficar centralizada em:

```text
blog-responsive.css
```

---

# Filosofia

O Blog da Coguis deve ser tratado como um produto digital.

Toda nova funcionalidade deve seguir os princípios:

- reutilização
- organização
- documentação
- escalabilidade
- manutenção simples

---

# Histórico

## v1.0

- Modularização completa do CSS.
- Criação do componente image-card.
- Separação por responsabilidades.
- Centralização da responsividade.
- Início da documentação oficial.