# Publicação no GitHub Pages

A aplicação está configurada para publicação automática no GitHub Pages com o workflow `.github/workflows/pages.yml`.

## Como funciona

1. Push na `main` dispara o workflow de deploy.
2. O pipeline executa `npm ci`, `npm run lint`, `npm test` e `npm run build`.
3. O conteúdo de `dist/` é enviado com `upload-pages-artifact`.
4. A publicação é concluída com `deploy-pages` no ambiente `github-pages`.

URL publicada: `https://herick721.github.io/grade-horaria-automatizada/`.

## Pré-requisitos

- Em **Settings → Pages**, manter **Build and deployment → Source → GitHub Actions**.
- Repositório público (ou plano compatível com Pages privado).
- `base` do Vite definido como `/grade-horaria-automatizada/` (já configurado em `vite.config.ts`).
