# 🍄 Arquitetura CSS — Site da Coguis Informática

> Documento oficial da arquitetura CSS do site institucional da Coguis Informática.

---

## Objetivo

Este documento descreve a organização do CSS do site institucional da Coguis Informática.

A arquitetura foi criada para manter o projeto organizado, escalável, fácil de manter e preparado para reutilização em futuros projetos da Coguis UI.

---

## Estrutura Geral

```text
css/
├── style.css
├── base/
│   ├── variables.css
│   └── base.css
├── components/
│   ├── button.css
│   ├── cards.css
│   ├── container.css
│   ├── sections.css
│   ├── tags.css
│   └── titles.css
├── layout/
│   ├── header.css
│   ├── footer.css
│   └── whatsapp.css
├── sections/
│   ├── home-hero.css
│   ├── trust.css
│   ├── manifesto.css
│   ├── services-showcase.css
│   ├── split-section.css
│   ├── social-proof.css
│   ├── web-services.css
│   ├── digital-showcase.css
│   ├── final-contact.css
│   └── responsive.css
└── blog/
```

---

## Arquivo Principal

O arquivo `style.css` deve funcionar apenas como gerenciador de imports.

Ele não deve conter regras CSS diretas.

---

## Camadas da Arquitetura

### 1. Base

Contém tokens, reset e estilos globais.

Arquivos:

- `variables.css`
- `base.css`

### 2. Components

Contém componentes reutilizáveis da Coguis UI.

Exemplos:

- botões;
- containers;
- títulos;
- tags;
- cards;
- estruturas de seção.

### 3. Layout

Contém estruturas fixas do site.

Exemplos:

- header;
- footer;
- botão flutuante do WhatsApp.

### 4. Sections

Contém seções específicas da Home.

Exemplos:

- Hero;
- Confiança;
- Serviços;
- Prova social;
- Contato final.

---

## Ordem dos Imports

```css
@import url("./base/variables.css");
@import url("./base/base.css");

@import url("./components/container.css");
@import url("./components/button.css");
@import url("./components/cards.css");
@import url("./components/titles.css");
@import url("./components/tags.css");
@import url("./components/sections.css");

@import url("./layout/header.css");
@import url("./layout/footer.css");
@import url("./layout/whatsapp.css");

@import url("./sections/home-hero.css");
@import url("./sections/trust.css");
@import url("./sections/manifesto.css");
@import url("./sections/services-showcase.css");
@import url("./sections/split-section.css");
@import url("./sections/social-proof.css");
@import url("./sections/web-services.css");
@import url("./sections/digital-showcase.css");
@import url("./sections/final-contact.css");
@import url("./sections/responsive.css");
```

---

## Responsabilidades dos Arquivos

### `base/variables.css`

Responsável pelos tokens visuais do projeto:

- cores;
- fontes;
- espaçamentos;
- radius;
- sombras;
- tamanhos máximos;
- transições.

### `base/base.css`

Responsável pelos estilos globais:

- reset básico;
- comportamento do `html`;
- estilo base do `body`;
- imagens;
- links;
- acessibilidade;
- classes utilitárias globais como `sr-only`.

### `components/`

Responsável por componentes reutilizáveis.

Exemplos:

- `button.css`;
- `container.css`;
- `titles.css`;
- `tags.css`;
- `cards.css`;
- `sections.css`.

### `layout/`

Responsável por estruturas fixas do site.

Exemplos:

- `header.css`;
- `footer.css`;
- `whatsapp.css`.

### `sections/`

Responsável por seções específicas da Home.

Cada seção deve ter seu próprio arquivo.

---

## Regras Oficiais

1. O `style.css` não deve receber CSS direto.
2. Componentes reutilizáveis devem ficar em `components/`.
3. Estruturas fixas devem ficar em `layout/`.
4. Seções da Home devem ficar em `sections/`.
5. Tokens visuais devem ficar em `base/variables.css`.
6. Ajustes responsivos da Home devem ficar em `sections/responsive.css`.
7. Nenhum arquivo deve misturar responsabilidades diferentes.
8. Antes de criar uma nova classe, verificar se já existe um componente reutilizável.
9. Toda nova estrutura relevante deve ser documentada.
10. Toda refatoração importante deve gerar commit.

---

## Filosofia

A arquitetura CSS da Coguis segue o princípio de responsabilidade única.

Cada arquivo deve responder claramente a uma pergunta:

> “Qual parte do site este arquivo controla?”

Se a resposta não for clara, o CSS provavelmente está no lugar errado.

---

## Fluxo de Carregamento

```text
Google Fonts
↓
Base
↓
Components
↓
Layout
↓
Sections
↓
Responsive
```

Essa ordem garante que:

- os tokens estejam disponíveis antes dos componentes;
- os componentes carreguem antes das seções;
- o layout seja carregado antes dos ajustes finais;
- a responsividade fique por último.

---

## Convenção de Manutenção

Ao criar uma nova funcionalidade visual:

1. Verificar se é um componente reutilizável.
2. Se for global, criar em `components/`.
3. Se for uma seção específica da Home, criar em `sections/`.
4. Se for uma estrutura fixa, criar em `layout/`.
5. Se for token visual, adicionar em `base/variables.css`.
6. Se for responsivo, adicionar em `sections/responsive.css`.

---

## Histórico

### v1.0

- Separação do `style.css` em camadas.
- Criação de `base/`.
- Criação de `components/`.
- Criação de `layout/`.
- Criação de `sections/`.
- Transformação do `style.css` em gerenciador de imports.
- Criação da base da Coguis UI.