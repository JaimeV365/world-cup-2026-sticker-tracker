# Traffic & analytics (Cloudflare)

Your site is hosted on **Cloudflare Pages**. You can see usage without Google Analytics.

---

## 1. Built-in Pages metrics (no setup)

Already available — no code changes.

1. Open [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Go to **Workers & Pages**
3. Click project **`wc2026-sticker-tracker`**
4. Open the **Metrics** tab (or project overview)

You will see:

- **Requests** — how many times pages were loaded
- **Bandwidth** — data served
- **Deployments** — when the site was updated

This is enough for a rough idea of traffic. It does not show detailed page views or countries unless you add Web Analytics below.

---

## 2. Cloudflare Web Analytics (recommended, still privacy-friendly)

Free, no cookies, no Google. Shows visits, page views, referrers, countries, devices.

### Enable it

1. Dashboard → **Analytics & Logs** → **Web Analytics**
2. Click **Add a site**
3. Enter: `wc2026-sticker-tracker.pages.dev`
4. Copy the **beacon token** Cloudflare gives you

### Add the token to this project

1. Open `index.html` in the repo
2. Find the commented block near the bottom (before `<script>`)
3. Uncomment the `<script defer src="...beacon.min.js"...>` line
4. Replace `YOUR_TOKEN_HERE` with your token
5. Optionally add the same script to `help.html`
6. Commit and push — Cloudflare redeploys in ~1 minute

### Update the privacy text (optional)

If you enable Web Analytics, the help page “no trackers” line is still mostly true — Cloudflare Web Analytics is cookieless and privacy-oriented — but you may want to add one sentence that anonymous visit counts are collected. Switch to Agent mode if you want that wording updated.

---

## What you do **not** need

- Google Analytics
- A paid Cloudflare plan (free tier is enough)
- Changes to GitHub — analytics run on the Cloudflare side or via one small script you add

---

## Live site

https://wc2026-sticker-tracker.pages.dev
