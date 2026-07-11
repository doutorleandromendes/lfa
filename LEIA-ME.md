# LFA Strip Analyzer — App de homescreen (GitHub Pages)

Esta pasta é um site estático autocontido. Publicando no GitHub Pages, você
tem uma URL HTTPS que funciona como app no iPhone (com câmera ao vivo).

## Arquivos
- `index.html`            — o app completo (câmera + preparo + análise + laudo)
- `manifest.webmanifest`  — configuração de PWA (nome, ícones, standalone)
- `apple-touch-icon.png`  — ícone iOS (180×180)
- `lfa-icon-192.png`      — ícone PWA
- `lfa-icon-512.png`      — ícone PWA / splash

Todas as referências são relativas — funcionam sob subcaminho do GitHub Pages.

---

## Como publicar (2 opções)

### Opção 1 — Repositório dedicado (mais limpo)

1. Crie um repo novo no GitHub, ex.: `lfa-analyzer`
2. Faça upload de TODOS os arquivos desta pasta na raiz do repo
3. No repo: Settings → Pages → em "Source" escolha `Deploy from a branch`,
   branch `main`, pasta `/ (root)` → Save
4. Aguarde ~1 min. A URL será:
   `https://SEU-USUARIO.github.io/lfa-analyzer/`

### Opção 2 — Dentro do repo `exames` (subpasta)

1. Crie uma pasta no repo `exames`, ex.: `lfa/`
2. Suba os arquivos desta pasta dentro de `exames/lfa/`
3. Se o Pages do `exames` já estiver ativo, a URL será:
   `https://SEU-USUARIO.github.io/exames/lfa/`
   (Se não estiver, ative em Settings → Pages como na Opção 1.)

---

## Adicionar à tela de início do iPhone

**Precisa ser no Safari** (não Chrome):

1. Abra a URL do Pages no Safari
2. Toque no botão Compartilhar (quadrado com seta ↑)
3. Role e toque em "Adicionar à Tela de Início"
4. Nome sugerido: "LFA" → Adicionar

O ícone aparece na homescreen. Ao abrir, roda em tela cheia (standalone),
sem barra do Safari, com a câmera ao vivo funcionando.

---

## Notas

- **Câmera ao vivo** exige HTTPS — o GitHub Pages já fornece. Funciona.
- **Primeira vez:** o Safari pede permissão de câmera. Se negar, o app cai no
  seletor de câmera nativo do iOS (fallback automático).
- **HEIC:** fotos tiradas fora do app (na câmera nativa do iOS) podem vir em
  HEIC — o app pede JPEG. Fotos tiradas DENTRO do app já saem em JPEG, sem
  problema.
- Nada é enviado para servidor: todo o processamento é no próprio aparelho.
