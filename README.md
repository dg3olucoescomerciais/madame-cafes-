# Madame Café’s — site institucional

Site estático da Madame Café’s. O conteúdo publicado fica em `dist/` e não exige instalação de dependências nem comando de compilação.

## Publicar no Cloudflare Workers com GitHub

O repositório está conectado ao projeto `madame-cafes` em Cloudflare Workers. O arquivo `wrangler.jsonc` aponta os recursos estáticos para `dist/` e permite que o comando de implantação `npx wrangler deploy` publique o site sem um script de aplicação.

Na configuração de Builds do Cloudflare, use o ramo `main`, diretório raiz `/`, comando de construção vazio e comando de implantação `npx wrangler deploy`. Cada alteração enviada a `main` cria uma nova implantação. A URL pública atual é `https://madame-cafes.dg3solucoescomerciais.workers.dev/`.

## Ao configurar um domínio próprio

Os endereços de SEO em `dist/index.html` (`canonical`, `og:url` e JSON-LD), `dist/robots.txt` e `dist/sitemap.xml` apontam para a URL `workers.dev`. Quando o domínio próprio estiver ativo e verificado, substitua essas ocorrências pela URL definitiva.

O arquivo `.openai/hosting.json` pertence à publicação atual no Sites; a implantação em Workers usa `wrangler.jsonc` e os arquivos de `dist/`. Nenhuma chave ou segredo é necessário para servir este site.
