# marcaosite — Landing page Marcão Vivacqua

Página única (sem rolagem), responsiva, em HTML + CSS puro. Sem dependências além da fonte do Google Fonts.

## Estrutura
```
marcaosite/
├── index.html          página principal
├── 404.html            página de erro
├── css/style.css       estilos
├── img/
│   ├── bg.jpg          fundo (otimizado, 1200px)
│   ├── logo.png        #agoraéMARCÃO!
│   ├── marcao.png      foto recortada
│   ├── favicon.png
│   └── og-image.jpg    prévia para WhatsApp/redes (1200x630)
├── robots.txt
├── sitemap.xml
├── site.webmanifest
└── .htaccess           cache, gzip e rota do 404 (Apache)
```

## Antes de publicar — trocar
1. **Domínio**: substituir `https://www.marcaovivacqua.com.br/` em `index.html` (canonical + og), `robots.txt` e `sitemap.xml`.
2. **WhatsApp**: `https://wa.me/5528999999999` → número real com DDI+DDD.
3. **Instagram e Facebook**: URLs reais dos perfis.
4. **Textos**: o título "Junto com a gente" e a linha de apoio são sugestões — ajustar ao discurso aprovado.
5. **`lastmod`** do `sitemap.xml` na data da publicação.

## Publicação
Subir o conteúdo da pasta na raiz do servidor (public_html). Funciona também em Vercel, Netlify ou Cloudflare Pages sem build — basta apontar para esta pasta.
