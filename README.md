# Zenitram Solutions

Public one-page site for **Zenitram Solutions** — network and systems solutions for houses of worship and nonprofit organizations.

## Stack

- [Astro](https://astro.build) 7 (static output)
- [Tailwind CSS](https://tailwindcss.com) v4 via `@tailwindcss/vite`
- [Starwind UI](https://starwind.dev) (Button, Card, Image)
- pnpm

## Develop

```bash
pnpm install
pnpm dev
```

## Build

```bash
pnpm build
pnpm preview
```

Requires Node.js `>=22.12.0`.

## Deploy

Cloudflare Workers (static assets) on account **ZenAgent**:

```bash
pnpm deploy
```

Requires `CLOUDFLARE_API_TOKEN` (or `CLOUDFLARE_MGMT_TOKEN`) and account id `1466bea799ef2ab86d6dd673941cc668`.

Pushes to `main` also deploy via `.github/workflows/deploy-cloudflare.yml` once repo secrets `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` are set.
