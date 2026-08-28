# Free website address (no payment)

Nobody offers free `.com` or `.dev` domains permanently. These two options give you a **free subdomain** with **no personal name** and **no cost**.

---

## Option A — Cloudflare Pages (recommended)

**Your new URL:** `https://wc2026-sticker-tracker.pages.dev`  
**Cost:** free  
**You are not creating a company** — just a free Cloudflare account (like Gmail).

GitHub keeps the code. Cloudflare serves the website at a neutral address.

### Setup (~5 minutes)

1. **Create a free Cloudflare account**  
   [https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

2. **Open Workers & Pages**  
   [https://dash.cloudflare.com/?to=/:account/workers-and-pages](https://dash.cloudflare.com/?to=/:account/workers-and-pages)

3. **Create application → Pages → Connect to Git**

4. **Connect GitHub** and allow access to the repo:  
   `JaimeV365/world-cup-2026-sticker-tracker`

5. **Use these settings:**

   | Setting | Value |
   |---------|--------|
   | Project name | `wc2026-sticker-tracker` |
   | Production branch | `main` |
   | Framework preset | **None** |
   | Build command | *(leave empty)* |
   | Build output directory | `.` |

6. Click **Save and Deploy**. Wait ~1 minute.

7. Your site is live at:  
   **`https://wc2026-sticker-tracker.pages.dev`**

Every time you `git push` to `main`, Cloudflare redeploys automatically.

### Optional: redirect old GitHub URL

The old link still works. Share the new `.pages.dev` link with collectors.

---

## Option B — GitHub project name (no Cloudflare)

**Your new URL:** `https://wc2026-sticker-tracker.github.io/`  
**Cost:** free  

This is **not** registering a business. On GitHub, an “Organization” is just a **neutral account name** for repos — many hobby projects use them.

### Setup

1. Create a free organization: [github.com/account/organizations/new](https://github.com/account/organizations/new)  
   - Choose the free plan  
   - Name: `wc2026-sticker-tracker`

2. Transfer the repo: repo **Settings → General → Transfer ownership** → select the new org

3. Rename the repo to exactly: **`wc2026-sticker-tracker.github.io`**

4. **Settings → Pages** → source: `main`, folder `/`

5. Site URL: **`https://wc2026-sticker-tracker.github.io/`**

---

## Which should I pick?

| | Cloudflare Pages | GitHub org site |
|---|------------------|-----------------|
| URL | `wc2026-sticker-tracker.pages.dev` | `wc2026-sticker-tracker.github.io` |
| Feels like | Separate hosting brand | Still GitHub, neutral name |
| Extra account | Cloudflare (free) | GitHub org (free) |
| Auto-deploy on push | Yes | Yes |

**If you don’t want anything called “organization”** → use **Cloudflare Pages (Option A)**.

---

## Current URL (until you switch)

https://jaimev365.github.io/world-cup-2026-sticker-tracker/

This keeps working. Switch when you’re ready, then share the new link.
