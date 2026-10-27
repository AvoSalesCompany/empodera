# Empodera Cosméticos

Site da loja **Empodera Cosméticos** (RS & SC) — perfumes de alta fixação inspirados nas grandes fragrâncias, com frete grátis para todo o Brasil.

O site é uma página única (`index.html`), sem dependências de build: catálogo, sacola de compras e pedido montado automaticamente para o **WhatsApp**, funcionando no computador e no celular.

## Como ver o site

Abra o arquivo `index.html` em qualquer navegador. Para publicar na internet, veja **Publicar com GitHub Pages** abaixo.

## O que dá para editar fácil

No final do `index.html`, dentro do `<script>`, há um bloco de configuração:

```js
var LOJA = {
  whatsapp: "5551999999999",   // ⚠️ número que recebe os pedidos (DDI+DDD+número, só dígitos)
  instagram: "https://www.instagram.com/empodera.rs.sc/",
  nome: "Empodera Cosméticos",
  pixChave: ""                 // opcional: chave Pix exibida no checkout
};

// Preços por tamanho (R$)
var PRECO = { "50": 69.90, "100": 99.90 };

// Lista de perfumes (nome, linha, inspiração, notas, descrição)
var PRODUTOS = [ ... ];
```

- **WhatsApp:** troque o número em `LOJA.whatsapp` (ex.: `5551999998888`).
- **Preços:** ajuste `PRECO`, ou dê um preço por perfume adicionando `preco50`/`preco100` em cada item.
- **Perfumes:** adicione, remova ou edite itens em `PRODUTOS`.
- **Cores:** todas em `:root`, no topo do `<style>` (`--violet`, `--gold`, `--bg`...).

## Recursos

- Catálogo com filtro Masculinos / Femininos e busca
- Ficha de cada perfume (tamanho 50/100 ml, notas, inspiração)
- Sacola com total ao vivo, salva no navegador
- Checkout que gera a mensagem do pedido pronta no WhatsApp
- Identidade da marca: preto + roxo, logo vetorizada, fontes de perfumaria
- Transição com a logo, animações ao rolar, FAQ e seção "Como comprar"
- Responsivo (celular e computador)

## Publicar com GitHub Pages

1. No GitHub: **Settings → Pages**.
2. Em *Build and deployment*, **Source: Deploy from a branch**.
3. Branch: **main**, pasta **/ (root)** → **Save**.
4. Em alguns minutos o site fica no ar em `https://avosalescompany.github.io/empodera/`.

## Arquivos

- `index.html` — o site inteiro (HTML, CSS e JS inline).
- `assets/logo.svg` — a logo da Empodera em vetor.
