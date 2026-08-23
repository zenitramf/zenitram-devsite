# Zenitram Solutions

Public one-page site for **Zenitram Solutions** — church-focused technology: websites, graphic design, media, staff portals, and Zenith Cast.

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

Cloudflare Workers (static assets) on account **Zenitram**, custom domains `zenitram.dev` / `www.zenitram.dev`:

```bash
pnpm deploy
```

Requires `CLOUDFLARE_API_TOKEN` (e.g. `CLOUDFLARE_MGMT_API`) and account id `23f99d3ef188b488e18827b853b73295`.

Git-linked deploys:

- **Cloudflare Workers Builds** trigger `Production Deploy` on `main` (build: `pnpm install --frozen-lockfile && pnpm build`, deploy: `npx wrangler deploy`)
- **GitHub Actions** `.github/workflows/deploy-cloudflare.yml` using repo secrets `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID`
