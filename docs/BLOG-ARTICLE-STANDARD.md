# 🍄 Padrão Oficial de Artigos — Blog da Coguis Informática

> Documento técnico e editorial oficial para criação, manutenção e publicação dos artigos do Blog da Coguis Informática.

---

## 1. Objetivo

Este documento estabelece o padrão obrigatório para todos os artigos publicados no Blog da Coguis Informática.

Seu objetivo é garantir:

- consistência visual;
- organização técnica;
- qualidade editorial;
- acessibilidade;
- otimização para mecanismos de busca;
- facilidade de manutenção;
- escalabilidade do Blog;
- preservação da identidade da Coguis Informática.

Todo novo artigo deve seguir este padrão e utilizar o template oficial como base.

---

## 2. Template Oficial

Todo artigo deve ser criado a partir do arquivo:

```text
blog/templates/article-template.html
```

Nunca criar um artigo a partir de um arquivo HTML vazio.

O fluxo correto é:

```text
Copiar article-template.html
↓
Colar em blog/artigos/
↓
Renomear o arquivo
↓
Preencher os metadados
↓
Substituir o conteúdo do template
↓
Adicionar imagens
↓
Validar responsividade
↓
Revisar SEO
↓
Adicionar o artigo ao Blog
↓
Publicar
```

---

## 3. Estrutura de Diretórios

A estrutura oficial do módulo Blog é:

```text
blog/
├── index.html
├── artigos/
│   ├── nome-do-artigo.html
│   └── outros-artigos.html
├── templates/
│   └── article-template.html
└── README.md
```

As imagens devem permanecer centralizadas na pasta global de imagens:

```text
images/
└── blog/
    └── artigos/
        └── nome-do-artigo/
            ├── hero.webp
            ├── imagem-01.webp
            ├── imagem-02.webp
            └── imagem-03.webp
```

---

## 4. Nomeação dos Arquivos

Os arquivos dos artigos devem utilizar URLs amigáveis.

### Regras

- utilizar apenas letras minúsculas;
- não utilizar acentos;
- não utilizar espaços;
- separar palavras com hífen;
- evitar nomes longos;
- utilizar termos relacionados à palavra-chave principal.

### Correto

```text
notebook-esquentando.html
ssd-ou-hd.html
como-aparecer-no-google.html
o-que-e-seo.html
como-criar-senhas-seguras.html
```

### Incorreto

```text
Notebook Esquentando.html
notebook_esquentando.html
artigo1.html
NOVO-ARTIGO.html
como-limpar-o-seu-notebook-de-forma-correta-e-segura.html
```

---

## 5. Nomeação das Pastas de Imagens

A pasta de imagens deve possuir o mesmo identificador principal do artigo.

Exemplo:

```text
Artigo:
blog/artigos/notebook-esquentando.html

Imagens:
images/blog/artigos/notebook-esquentando/
```

Conteúdo esperado:

```text
notebook-esquentando/
├── hero.webp
├── imagem-01.webp
├── imagem-02.webp
└── imagem-03.webp
```

A imagem principal deve sempre utilizar o nome:

```text
hero.webp
```

---

## 6. Caminhos Relativos

Os artigos ficam dentro de:

```text
blog/artigos/
```

Por isso, os arquivos globais devem utilizar dois níveis de retorno.

### CSS

```html
<link rel="stylesheet" href="../../css/style.css">
<link rel="stylesheet" href="../../css/blog.css">
<link rel="stylesheet" href="../../css/article.css">
```

### JavaScript

```html
<script src="../../js/script.js"></script>
```

### Imagens

```html
<img src="../../images/blog/artigos/nome-do-artigo/hero.webp" alt="">
```

### Página inicial

```html
<a href="../../index.html">Início</a>
```

### Página principal do Blog

```html
<a href="../">Blog</a>
```

---

## 7. SEO Principal

Todo artigo deve possuir metadados próprios.

Nenhum placeholder do template pode permanecer no artigo publicado.

---

## 8. Title

O elemento `<title>` deve informar o assunto principal do artigo e a marca.

Exemplo:

```html
<title>Notebook esquentando: causas e soluções | Blog da Coguis Informática</title>
```

### Regras

- incluir a palavra-chave principal;
- representar corretamente o conteúdo;
- evitar títulos genéricos;
- não repetir títulos já publicados;
- manter o nome da Coguis no final.

---

## 9. Meta Description

A meta description deve resumir o artigo e incentivar o clique.

Exemplo:

```html
<meta name="description"
    content="Entenda por que o notebook esquenta, quais sinais exigem atenção e como evitar problemas de temperatura e desempenho.">
```

### Regras

- escrever de forma natural;
- incluir a palavra-chave principal;
- explicar o benefício do artigo;
- evitar listas artificiais de palavras-chave;
- manter aproximadamente entre 140 e 160 caracteres.

---

## 10. Canonical

Todo artigo deve possuir uma URL canônica absoluta.

Exemplo:

```html
<link rel="canonical"
    href="https://coguisinformatica.github.io/coguisinformatica-site-coguis/blog/artigos/notebook-esquentando.html">
```

A mesma URL deve ser utilizada em:

- canonical;
- `og:url`;
- `mainEntityOfPage`;
- sitemap.

---

## 11. Open Graph

Todo artigo deve conter metadados para compartilhamento.

Exemplo:

```html
<meta property="og:type" content="article">
<meta property="og:locale" content="pt_BR">
<meta property="og:site_name" content="Coguis Informática">
<meta property="og:title" content="Notebook esquentando: causas e soluções">
<meta property="og:description"
    content="Descubra as causas do superaquecimento e saiba quando procurar assistência técnica.">
<meta property="og:url"
    content="https://coguisinformatica.github.io/coguisinformatica-site-coguis/blog/artigos/notebook-esquentando.html">
<meta property="og:image"
    content="https://coguisinformatica.github.io/coguisinformatica-site-coguis/images/blog/artigos/notebook-esquentando/hero.webp">
```

---

## 12. Twitter Card

Todo artigo deve possuir:

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Notebook esquentando: causas e soluções">
<meta name="twitter:description"
    content="Entenda as causas do superaquecimento e veja como proteger seu equipamento.">
<meta name="twitter:image"
    content="https://coguisinformatica.github.io/coguisinformatica-site-coguis/images/blog/artigos/notebook-esquentando/hero.webp">
```

---

## 13. Datas

As datas devem utilizar o padrão ISO nos metadados:

```html
<meta property="article:published_time" content="2026-07-10">
<meta property="article:modified_time" content="2026-07-10">
```

No conteúdo visual:

```html
<time datetime="2026-07-10">
    10 de julho de 2026
</time>
```

### Regras

- `published_time` representa a primeira publicação;
- `modified_time` deve ser atualizado quando houver alteração relevante;
- correções pequenas de ortografia não exigem alteração da data;
- atualizações técnicas ou editoriais importantes devem atualizar `modified_time`.

---

## 14. Dados Estruturados

Todo artigo deve utilizar `BlogPosting`.

Campos obrigatórios:

- `headline`;
- `description`;
- `image`;
- `datePublished`;
- `dateModified`;
- `author`;
- `publisher`;
- `mainEntityOfPage`.

Exemplo:

```html
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "BlogPosting",
    "headline": "Notebook esquentando: causas e soluções",
    "description": "Entenda as causas do superaquecimento e saiba como proteger seu notebook.",
    "image": [
        "https://coguisinformatica.github.io/coguisinformatica-site-coguis/images/blog/artigos/notebook-esquentando/hero.webp"
    ],
    "datePublished": "2026-07-10",
    "dateModified": "2026-07-10",
    "author": {
        "@type": "Organization",
        "name": "Coguis Informática",
        "url": "https://coguisinformatica.github.io/coguisinformatica-site-coguis/"
    },
    "publisher": {
        "@type": "Organization",
        "name": "Coguis Informática",
        "logo": {
            "@type": "ImageObject",
            "url": "https://coguisinformatica.github.io/coguisinformatica-site-coguis/images/logoCoguis.png"
        }
    },
    "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://coguisinformatica.github.io/coguisinformatica-site-coguis/blog/artigos/notebook-esquentando.html"
    }
}
</script>
```

---

## 15. Estrutura Obrigatória do Artigo

Todo artigo deve possuir:

1. breadcrumb;
2. categoria;
3. título principal;
4. resumo;
5. autor;
6. data de publicação;
7. tempo de leitura;
8. imagem principal;
9. introdução;
10. explicação do problema;
11. solução;
12. dicas práticas;
13. orientação sobre assistência profissional;
14. Dica do Coguis;
15. integração com Meu Site de Estudos, quando aplicável;
16. conclusão;
17. CTA;
18. FAQ;
19. artigos relacionados;
20. footer.

---

## 16. Breadcrumb

O breadcrumb deve representar a posição do artigo no site.

Exemplo:

```text
Início / Blog / Manutenção / Notebook esquentando
```

HTML:

```html
<nav class="article-breadcrumb container" aria-label="Navegação estrutural">
    <ol class="article-breadcrumb__list">
        <li><a href="../../index.html">Início</a></li>
        <li><a href="../">Blog</a></li>
        <li><a href="../#categorias">Manutenção</a></li>
        <li aria-current="page">Notebook esquentando</li>
    </ol>
</nav>
```

---

## 17. Categoria

A categoria deve ser exibida antes do título.

Exemplo:

```html
<a class="post-category" href="../#categorias">
    Manutenção
</a>
```

Utilizar apenas categorias oficiais do Blog.

---

## 18. Título Principal

Cada artigo deve possuir apenas um `<h1>`.

Exemplo:

```html
<h1 class="article-hero__title">
    Notebook esquentando: entenda as causas e saiba o que fazer
</h1>
```

### Regras

- apenas um H1 por artigo;
- utilizar a palavra-chave principal;
- evitar títulos muito extensos;
- representar fielmente o conteúdo;
- não utilizar título enganoso.

---

## 19. Resumo

O resumo deve explicar o que será abordado.

Exemplo:

```html
<p class="article-hero__summary">
    Entenda por que o notebook pode esquentar, quais sinais exigem atenção e como evitar problemas de desempenho e temperatura.
</p>
```

O resumo não deve repetir exatamente a meta description.

---

## 20. Metadados Visuais

O artigo deve exibir:

- autor;
- data;
- tempo de leitura.

Exemplo:

```html
<div class="article-meta">
    <span>Por <strong>Coguis Informática</strong></span>
    <span>
        Publicado em
        <time datetime="2026-07-10">10 de julho de 2026</time>
    </span>
    <span>6 min de leitura</span>
</div>
```

---

## 21. Tempo de Leitura

O tempo de leitura deve ser calculado com base aproximada em 200 palavras por minuto.

Exemplo:

```text
1.000 palavras ÷ 200 = 5 minutos
```

Apresentação:

```text
5 min de leitura
```

Arredondar para cima quando necessário.

---

## 22. Imagem Principal

A imagem principal deve utilizar:

```text
hero.webp
```

Exemplo:

```html
<img src="../../images/blog/artigos/notebook-esquentando/hero.webp"
    alt="Mascote Coguis analisando um notebook com sinais de superaquecimento">
```

### Regras

- utilizar formato WebP sempre que possível;
- manter boa qualidade visual;
- otimizar o tamanho do arquivo;
- usar texto alternativo descritivo;
- não iniciar o `alt` com “imagem de”;
- não repetir palavras-chave artificialmente.

---

## 23. Hierarquia dos Títulos

### H1

Utilizado uma única vez no título principal.

### H2

Utilizado nas principais seções do artigo.

Exemplos:

```text
Por que o notebook esquenta?
Como reduzir a temperatura?
Quando procurar assistência técnica?
```

### H3

Utilizado para subdivisões de um H2.

Exemplo:

```text
Acúmulo de poeira
Pasta térmica ressecada
Problemas no sistema de refrigeração
```

Nunca pular diretamente de H1 para H3.

---

## 24. Introdução

A introdução deve:

- apresentar o assunto;
- explicar o problema;
- mostrar a importância do tema;
- informar o que o leitor aprenderá;
- evitar excesso de contexto desnecessário.

A introdução deve ser direta e preferencialmente possuir entre dois e quatro parágrafos curtos.

---

## 25. Explicação do Problema

Esta seção deve abordar:

- sintomas;
- causas;
- consequências;
- erros comuns;
- situações que merecem atenção.

A linguagem deve ser acessível para pessoas sem formação técnica.

---

## 26. Solução

A seção de solução deve:

- apresentar orientações seguras;
- explicar limites de ações caseiras;
- evitar instruções perigosas;
- diferenciar prevenção de reparo técnico;
- informar quando a assistência profissional é necessária.

---

## 27. Dicas Práticas

As dicas devem ser apresentadas de forma clara.

Exemplo:

```html
<ul>
    <li>Utilize o notebook sobre superfícies planas e firmes.</li>
    <li>Evite bloquear as entradas e saídas de ventilação.</li>
    <li>Realize limpeza preventiva periodicamente.</li>
</ul>
```

Não utilizar listas apenas para aumentar artificialmente o tamanho do artigo.

---

## 28. Imagens Intermediárias

As imagens internas devem seguir a sequência:

```text
imagem-01.webp
imagem-02.webp
imagem-03.webp
```

Exemplo:

```html
<figure class="article-content__media">
    <img src="../../images/blog/artigos/notebook-esquentando/imagem-01.webp"
        alt="Saídas de ventilação localizadas na parte inferior de um notebook">
    <figcaption>
        As entradas de ventilação não devem ficar bloqueadas durante o uso.
    </figcaption>
</figure>
```

Utilizar legendas quando elas agregarem contexto.

---

## 29. Quando Procurar Assistência

Todo artigo relacionado a manutenção, segurança, hardware ou software deve explicar quando o leitor deve procurar um profissional.

Esta seção deve evitar alarmismo.

Exemplo:

```text
Procure assistência quando o equipamento desligar sozinho, apresentar ruídos incomuns, aquecer excessivamente ou perder desempenho com frequência.
```

---

## 30. Dica do Coguis

Todo artigo deve incluir o bloco oficial:

```html
<aside class="coguis-tip" aria-labelledby="dica-coguis-titulo">
    <p class="eyebrow">Dica do Coguis</p>
    <h2 id="dica-coguis-titulo">🍄 Dica do Coguis</h2>
    <p>
        Nunca utilize o notebook sobre cobertores ou travesseiros, pois eles podem bloquear a ventilação.
    </p>
</aside>
```

### Características

- curta;
- útil;
- relacionada ao conteúdo;
- fácil de lembrar;
- sem repetição do restante do artigo.

---

## 31. Meu Site de Estudos

O bloco deve ser utilizado quando o artigo abordar:

- programação;
- desenvolvimento web;
- banco de dados;
- Linux;
- Git;
- GitHub;
- JavaScript;
- tecnologias estudadas pelo autor.

Exemplo:

```html
<aside class="study-reference" aria-labelledby="estudos-titulo">
    <p class="eyebrow">Aprenda na prática</p>
    <h2 id="estudos-titulo">Quer aprender como isso funciona?</h2>
    <p>
        Conheça também o projeto Meu Site de Estudos, onde compartilho conteúdos sobre programação, banco de dados, Linux, GitHub e desenvolvimento web.
    </p>
    <a class="button button--secondary"
        href="URL-OFICIAL-DO-MEU-SITE-DE-ESTUDOS"
        target="_blank"
        rel="noopener noreferrer">
        Conhecer o Meu Site de Estudos
    </a>
</aside>
```

Esse bloco não é obrigatório em artigos que não possuam relação com estudos ou desenvolvimento.

---

## 32. Conclusão

A conclusão deve:

- resumir os pontos principais;
- reforçar a orientação mais importante;
- evitar introduzir assuntos novos;
- preparar o leitor para a CTA.

---

## 33. CTA

Todo artigo deve possuir uma chamada para ação.

Exemplo:

```html
<aside class="article-cta" aria-labelledby="cta-artigo-titulo">
    <p class="eyebrow">Precisa de ajuda?</p>
    <h2 id="cta-artigo-titulo">
        A Coguis Informática pode ajudar.
    </h2>
    <p>
        Fale conosco para solicitar atendimento ou encontrar a melhor solução para seu computador, notebook ou presença digital.
    </p>
    <a class="button button--primary"
        href="https://wa.me/5511960281070"
        target="_blank"
        rel="noopener noreferrer">
        Falar com a Coguis
    </a>
</aside>
```

### Regras

- relacionar a CTA ao assunto do artigo;
- utilizar linguagem clara;
- evitar pressão comercial;
- usar o canal oficial;
- conferir o link antes da publicação.

---

## 34. FAQ

Cada artigo deve possuir entre três e cinco perguntas frequentes.

Exemplo:

```html
<section class="article-faq" aria-labelledby="faq-artigo-titulo">
    <h2 id="faq-artigo-titulo">Perguntas frequentes</h2>

    <details>
        <summary>É normal o notebook esquentar?</summary>
        <p>
            Um leve aquecimento pode ser normal durante o uso, mas temperaturas excessivas ou desligamentos precisam ser investigados.
        </p>
    </details>
</section>
```

As respostas devem ser:

- objetivas;
- claras;
- relacionadas à intenção de busca;
- consistentes com o conteúdo do artigo.

---

## 35. FAQ em Dados Estruturados

O uso de schema `FAQPage` deve ser avaliado antes de cada publicação.

As perguntas estruturadas devem corresponder exatamente ao conteúdo visível no artigo.

Não criar perguntas apenas para dados estruturados.

---

## 36. Artigos Relacionados

Todo artigo deve exibir até três conteúdos relacionados.

Os artigos devem possuir relação real com o assunto.

Exemplo:

```text
Artigo atual:
Notebook esquentando

Relacionados:
Como limpar o notebook
Quando trocar a pasta térmica
Cooler fazendo barulho
```

Evitar relacionar conteúdos apenas por conveniência.

---

## 37. Links Internos

Todo artigo deve incluir links internos quando fizer sentido.

Podem apontar para:

- outros artigos;
- página de serviços;
- página de contato;
- página inicial do Blog;
- Meu Site de Estudos.

Os textos dos links devem ser descritivos.

### Correto

```html
<a href="ssd-ou-hd.html">entenda as diferenças entre HD e SSD</a>
```

### Evitar

```html
<a href="ssd-ou-hd.html">clique aqui</a>
```

---

## 38. Links Externos

Links externos devem apontar para fontes confiáveis.

Quando abrirem uma nova aba:

```html
target="_blank" rel="noopener noreferrer"
```

Evitar excesso de links externos.

---

## 39. Texto Alternativo

Toda imagem informativa deve possuir `alt`.

### Correto

```html
alt="Mascote Coguis analisando as saídas de ventilação de um notebook"
```

### Incorreto

```html
alt="imagem"
```

Imagens puramente decorativas podem utilizar:

```html
alt=""
```

---

## 40. Linguagem

A linguagem dos artigos deve ser:

- clara;
- profissional;
- humanizada;
- acolhedora;
- objetiva;
- acessível.

Evitar:

- jargões sem explicação;
- excesso de siglas;
- tom alarmista;
- afirmações sem fundamento;
- linguagem agressiva;
- excesso de informalidade;
- exagero promocional.

---

## 41. Parágrafos

Os parágrafos devem ser curtos e confortáveis para leitura em telas.

Recomendação:

- uma ideia principal por parágrafo;
- evitar grandes blocos de texto;
- utilizar subtítulos para separar temas;
- utilizar listas somente quando elas melhorarem a compreensão.

---

## 42. Palavras-chave

Cada artigo deve possuir:

- uma palavra-chave principal;
- palavras-chave secundárias;
- termos relacionados;
- perguntas reais dos usuários.

A palavra-chave principal deve aparecer naturalmente em:

- title;
- meta description;
- H1;
- introdução;
- pelo menos um H2, quando natural;
- URL;
- texto alternativo, quando relevante.

Nunca repetir palavras-chave de forma artificial.

---

## 43. Categorias Oficiais

As categorias oficiais do Blog são:

- Manutenção;
- Presença Digital;
- Segurança;
- Dicas;
- Bastidores do Coguis;
- Meu Site de Estudos;
- Tecnologia Explicada.

Todo artigo deve pertencer a uma categoria principal.

---

## 44. Identificadores HTML

Os atributos `id` devem:

- utilizar letras minúsculas;
- não possuir acentos;
- utilizar hífen;
- ser únicos na página.

Exemplo:

```html
<h2 id="quando-procurar-assistencia">
    Quando procurar assistência técnica
</h2>
```

---

## 45. Acessibilidade

Antes da publicação, verificar:

- hierarquia correta de títulos;
- um único H1;
- textos alternativos;
- contraste;
- foco visível;
- links descritivos;
- botões compreensíveis;
- `aria-labelledby`;
- `aria-current`;
- navegação por teclado;
- FAQ com `details` e `summary`.

---

## 46. Responsividade

O artigo deve ser testado em:

- desktop;
- tablet;
- celular.

Verificar:

- título;
- breadcrumb;
- metadados;
- imagem Hero;
- largura dos parágrafos;
- listas;
- tabelas;
- botões;
- FAQ;
- artigos relacionados;
- footer;
- botão flutuante do WhatsApp.

---

## 47. Performance

Antes da publicação:

- otimizar imagens;
- evitar imagens excessivamente grandes;
- utilizar `loading="lazy"` nas imagens abaixo da dobra;
- utilizar `decoding="async"` quando apropriado;
- evitar JavaScript desnecessário;
- validar caminhos;
- remover placeholders e recursos não utilizados.

A imagem Hero pode ser carregada sem `loading="lazy"` quando for o principal elemento visual da página.

---

## 48. Atualização da Página Principal do Blog

Após criar o artigo, atualizar:

```text
blog/index.html
```

O artigo pode ser incluído em:

- artigo em destaque;
- últimos artigos;
- categoria correspondente;
- artigos mais recentes.

O card deve apontar para:

```text
artigos/nome-do-artigo.html
```

---

## 49. Atualização dos Artigos Relacionados

Ao publicar um artigo novo:

- adicionar relacionados no próprio artigo;
- avaliar artigos antigos que também podem apontar para o novo conteúdo;
- evitar links quebrados;
- manter coerência temática.

---

## 50. Atualização do Sitemap

Todo artigo publicado deve ser incluído no sitemap do projeto.

Exemplo:

```xml
<url>
    <loc>https://coguisinformatica.github.io/coguisinformatica-site-coguis/blog/artigos/notebook-esquentando.html</loc>
    <lastmod>2026-07-10</lastmod>
</url>
```

---

## 51. Indexação

Antes de solicitar indexação:

- confirmar que o artigo está publicado;
- abrir a URL pública;
- verificar o canonical;
- conferir o status HTTP;
- testar em dispositivo móvel;
- validar dados estruturados;
- revisar title e description.

---

## 52. Revisão Editorial

A revisão deve verificar:

- ortografia;
- clareza;
- coerência;
- repetições;
- afirmações técnicas;
- organização dos subtítulos;
- tom de voz;
- conclusão;
- CTA;
- FAQ.

---

## 53. Checklist Técnico

Antes da publicação:

- [ ] O artigo foi criado a partir do template oficial.
- [ ] O arquivo possui URL amigável.
- [ ] A pasta de imagens possui o mesmo nome do artigo.
- [ ] Todos os placeholders foram substituídos.
- [ ] O title está correto.
- [ ] A meta description está preenchida.
- [ ] O canonical está correto.
- [ ] Open Graph está completo.
- [ ] Twitter Card está completa.
- [ ] Os dados estruturados estão válidos.
- [ ] As datas estão corretas.
- [ ] Existe apenas um H1.
- [ ] A hierarquia H2 e H3 está correta.
- [ ] As imagens possuem texto alternativo.
- [ ] Os links internos funcionam.
- [ ] Os links externos funcionam.
- [ ] A CTA funciona.
- [ ] O FAQ está preenchido.
- [ ] Os artigos relacionados estão configurados.
- [ ] O artigo está responsivo.
- [ ] O sitemap foi atualizado.
- [ ] O artigo foi adicionado à página principal do Blog.

---

## 54. Checklist Editorial

Antes da publicação:

- [ ] O artigo responde uma dúvida real.
- [ ] A introdução é objetiva.
- [ ] A linguagem está acessível.
- [ ] Os parágrafos estão curtos.
- [ ] Os títulos representam o conteúdo.
- [ ] Não existem repetições desnecessárias.
- [ ] A Dica do Coguis agrega valor.
- [ ] A conclusão resume o artigo.
- [ ] A CTA está relacionada ao tema.
- [ ] O conteúdo foi revisado.

---

## 55. Status dos Artigos

Os artigos podem possuir os seguintes estados internos:

```text
Rascunho
Em revisão
Aguardando imagens
Pronto para publicação
Publicado
Atualização necessária
Arquivado
```

Esse status pode ser registrado na documentação interna ou no controle de produção de conteúdo.

---

## 56. Controle de Atualizações

Artigos publicados devem ser revisados quando:

- o conteúdo técnico mudar;
- ferramentas ou versões forem atualizadas;
- links deixarem de funcionar;
- informações comerciais mudarem;
- o artigo perder relevância;
- surgirem novos conteúdos relacionados.

---

## 57. Regra de Manutenção

O template oficial deve ser atualizado quando surgir uma melhoria que deva valer para todos os artigos futuros.

Artigos antigos devem ser atualizados gradualmente quando a alteração for importante para:

- SEO;
- acessibilidade;
- segurança;
- experiência do usuário;
- identidade visual.

---

## 58. Versão do Padrão

**Documento:** Padrão Oficial de Artigos  
**Arquivo:** `BLOG-ARTICLE-STANDARD.md`  
**Versão:** 1.0  
**Status:** Oficial  
**Ano:** 2026  

---

## 59. Histórico

### v1.0

- criação do padrão oficial;
- definição da estrutura de arquivos;
- definição dos requisitos de SEO;
- padronização do conteúdo editorial;
- criação dos checklists;
- integração com o template oficial;
- definição do fluxo de publicação.

---

## 60. Considerações Finais

O Blog da Coguis Informática deve ser tratado como um ativo digital permanente.

Cada artigo deve contribuir para:

- gerar tráfego orgânico;
- fortalecer a autoridade da marca;
- ajudar pessoas;
- atrair clientes;
- apoiar os serviços da Coguis;
- alimentar outros canais de conteúdo;
- preservar o conhecimento técnico da empresa.

A consistência entre os artigos é tão importante quanto a qualidade individual de cada publicação.

Todo artigo deve fortalecer a identidade, a confiança e o posicionamento da Coguis Informática.

---

**Coguis Informática**

**Tecnologia que vai até você.**

© 2026 Coguis Informática. Todos os direitos reservados.