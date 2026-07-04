# Sweeney Todd — Programa (Flipbook)

Programa digital interativo do espetáculo **Sweeney Todd**, em formato flipbook
(vira-páginas horizontal), com as páginas renderizadas em HTML vivo e animações
sutis por página.

## Conteúdo desta pasta

```
index.html        ← a página (o GitHub Pages abre este arquivo sozinho)
assets/           ← imagens usadas (capa, elenco, texturas, logos)
.nojekyll         ← desliga o processamento Jekyll do GitHub Pages
README.md         ← este arquivo
```

> Esta pasta é **autossuficiente** para hospedar. Não precisa de mais nada do
> projeto original (o editor `design-canvas.jsx`, `image-slot.js` e as pastas
> `flat-E/`, `screenshots/`, `uploads/` **não** são necessários).

## Requisito

A página carrega **React, Babel e as fontes (Google Fonts) via CDN**, então o
navegador do espectador precisa de **internet**. O GitHub Pages serve por HTTPS,
e todos os CDNs são HTTPS — funciona sem configuração extra.

## Como publicar no GitHub Pages

### Opção A — pelo site do GitHub (sem instalar nada)

1. Crie um repositório novo em <https://github.com/new> (ex.: `sweeney-programa`).
   Pode ser **público** (Pages é grátis em repositório público).
2. Na página do repositório: **Add file → Upload files**.
3. Arraste **o conteúdo desta pasta** (o `index.html`, a pasta `assets/` e o
   `.nojekyll`) — e **não** a pasta `github` em si. O `index.html` tem que ficar
   na raiz do repositório.
4. **Commit changes**.
5. Vá em **Settings → Pages**.
6. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
7. Em **Branch**, selecione `main` e a pasta `/ (root)` → **Save**.
8. Aguarde ~1 minuto. O endereço aparece no topo da página Pages:
   `https://SEU-USUARIO.github.io/sweeney-programa/`

### Opção B — pela linha de comando (git)

Rode dentro **desta pasta** (`github/`):

```bash
git init
git add .
git commit -m "Programa Sweeney Todd - flipbook"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/sweeney-programa.git
git push -u origin main
```

Depois faça os passos **5 a 8** da Opção A para ativar o Pages.

## Observações

- Os caminhos das imagens são **relativos** (`assets/...`), então o site
  funciona mesmo publicado em subpasta (`usuario.github.io/repositorio/`).
- Para trocar uma foto do elenco, substitua o arquivo correspondente em
  `assets/cast/` mantendo o mesmo nome.
