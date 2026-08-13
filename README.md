# marcaosite — Landing page Marcão Vivacqua

Página única (sem rolagem), responsiva, em HTML + CSS puro. Sem dependências além da fonte do Google Fonts.

**Somente imagem**: a página não exibe nenhum texto além da linha legal do rodapé
(nome completo + CNPJ). Logo `#agoraéMARCÃO!` e foto são imagens.

## Estrutura
```
marcaosite/
├── index.html          página principal (logo + foto + rodapé legal)
├── 404.html            página de erro (logo clicável, redireciona para / em 4s)
├── css/style.css       estilos
├── img/
│   ├── bg.jpg          fundo — montagem vertical 1200x1852
│   ├── logo.png        #agoraéMARCÃO! (962x206)
│   ├── marcao.png      foto recortada (433x734)
│   ├── favicon.png
│   └── og-image.jpg    prévia para WhatsApp/redes (1200x630)
├── robots.txt
├── sitemap.xml
├── site.webmanifest
└── .htaccess           cache, gzip e rota do 404 (Apache)
```

## Fundo em duas camadas
O `bg.jpg` é vertical; em telas largas o `cover` estouraria o zoom. Solução em `css/style.css`:
- `body::before` — a própria imagem em `cover`, borrada (`blur 28px`): preenche 100% da tela;
- `body::after` — a montagem nítida dimensionada pela altura (`auto 118%`), com `mask-image`
  alinhada à borda real da imagem (`calc(50% ± 37vh)`) para fundir as laterais sem corte seco.

## Antes de publicar — trocar
1. **Domínio**: substituir `https://www.marcaovivacqua.com.br/` em `index.html` (canonical + og), `robots.txt` e `sitemap.xml`.
2. **`lastmod`** do `sitemap.xml` na data da publicação.

## Publicação
Subir o conteúdo da pasta na raiz do servidor (public_html). Funciona também em Vercel, Netlify ou Cloudflare Pages sem build — basta apontar para esta pasta (nesse caso o `.htaccess` é ignorado; cache/404 são automáticos nessas plataformas).

Repositório: https://github.com/morroalto/marcaosite
