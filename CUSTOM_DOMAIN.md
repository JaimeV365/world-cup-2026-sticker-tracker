# Custom domain setup

The default GitHub Pages URL includes your GitHub username. To use a neutral address, pick **one** of these options.

---

## Option A — Custom domain (recommended for sharing)

**Cost:** about £10–15 / year for a `.dev` or `.com` name  
**Example URLs:** `wc2026stickers.dev`, `stickeralbum2026.dev`

You do **not** need Cloudflare for hosting. GitHub Pages still hosts the site. Cloudflare (or any registrar) is only where you **buy the name** and point DNS.

### 1. Buy a domain

Register at any provider, for example:

- [Cloudflare Registrar](https://www.cloudflare.com/products/registrar/) — at-cost pricing
- [Porkbun](https://porkbun.com), [Namecheap](https://namecheap.com), etc.

Search for something neutral (avoid trademark names).

### 2. Tell GitHub your domain

1. Open repo **Settings → Pages → Custom domain**
2. Enter your domain (e.g. `wc2026stickers.dev`)
3. Wait for DNS check (can take up to 24 hours)

### 3. Add DNS records at your registrar

**If using the root domain** (`wc2026stickers.dev`):

| Type | Name | Value |
|------|------|-------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

**If using `www`** (`www.wc2026stickers.dev`):

| Type | Name | Value |
|------|------|-------|
| CNAME | `www` | `jaimev365.github.io` |

On **Cloudflare**: set the record to **DNS only** (grey cloud), not proxied, until GitHub verifies.

### 4. Add CNAME file to this repo

Create a file named `CNAME` (no extension) in the repo root containing **only** your domain:

```
wc2026stickers.dev
```

Commit and push. GitHub Pages will serve the site at that address.

### 5. Enable HTTPS

In **Settings → Pages**, enable **Enforce HTTPS** once the certificate is ready.

---

## Option B — GitHub Organization (free, no custom domain)

**Cost:** free  
**Example URL:** `https://wc2026-sticker-tracker.github.io/`

Your personal username is not in the URL. The org name is visible instead.

### Steps

1. Create a free organization: [github.com/account/organizations/new](https://github.com/account/organizations/new)  
   - Name idea: `wc2026-sticker-tracker`
2. Transfer this repository to the organization (repo **Settings → General → Transfer ownership**)
3. Rename the repo to **`wc2026-sticker-tracker.github.io`** (exact name = org name + `.github.io`)
4. **Settings → Pages** → deploy from `main` branch, root `/`
5. Site URL becomes: `https://wc2026-sticker-tracker.github.io/`

Update any links you have shared to the new URL.

---

## Do you need Cloudflare?

| Service | Required? |
|---------|-----------|
| **GitHub Pages** | Yes — hosts the website |
| **Cloudflare / registrar** | Only if you buy a custom domain |
| **Cloudflare CDN** | Optional — not needed for this small static site |

---

## Current default URL

https://jaimev365.github.io/world-cup-2026-sticker-tracker/

This works until you switch to Option A or B. Old links keep working unless you delete the personal repo copy.
