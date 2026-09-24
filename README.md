# Madame Café’s — site institucional

Site estático da Madame Café’s. O conteúdo publicado fica em `dist/` e não exige instalação de dependências nem comando de compilação.

## Publicar no Cloudflare Pages com GitHub

1. Envie esta pasta a um repositório GitHub, usando `main` como ramo de produção.
2. Em **Workers & Pages → Create application → Pages → Connect to Git**, selecione o repositório.
3. Configure **Framework preset: None**, **Build command: vazio**, **Build output directory: `dist`**, **Root directory: raiz do repositório** e **Production branch: `main`**.
4. Publique e confira a URL de produção `*.pages.dev` informada pelo Cloudflare. Os próximos envios ao ramo de produção serão implantados automaticamente.

## Antes de divulgar a nova URL

Os endereços de SEO em `dist/index.html` (`canonical`, `og:url` e JSON-LD), `dist/robots.txt` e `dist/sitemap.xml` ainda apontam para a URL já publicada no Sites. Substitua **todas** as ocorrências de `https://madame-cafes.espa-o-de-tr-3832.chatgpt.site/` pela URL definitiva do Cloudflare Pages ou pelo domínio próprio, após verificá-lo. Confirme também que as imagens, o link de WhatsApp e o Instagram abrem corretamente na nova hospedagem.

O arquivo `.openai/hosting.json` pertence à publicação atual no Sites; o Cloudflare Pages usa apenas os arquivos de `dist/`. Nenhuma chave ou segredo é necessário para servir este site.
