# HANLURE · Cognitive Allure

A minimal, no-dependency landing page for **hanlure.com** with an AI-aesthetic neon style.

- Single file: `index.html`
- No external assets, instant GitHub Pages / Cloudflare Pages deploy
- Bilingual copy (EN + 中文) and an affiliation disclaimer

## Quick Deploy (GitHub Pages)

1. Create a repository, e.g. `hanlure-site`.
2. Add `index.html` from this package and commit.
3. In **Settings → Pages**:
   - Build from a **branch** (main) and root (`/`).
   - Save, wait until the Pages URL shows up (e.g. `https://<user>.github.io/hanlure-site/`).
4. Click **Add custom domain**, enter `hanlure.com`, and enable **Enforce HTTPS**.
5. Go to your domain registrar (e.g. 22.cn) and add DNS records:
   - **A**: `hanlure.com` → 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153  (GitHub Pages IPv4)
   - **CNAME**: `www.hanlure.com` → `<user>.github.io.`
   - (Optional) `CNAME` flattening is not needed at GitHub; apex uses A records above.

> 22.cn path: 登录 → 域名 → 解析设置 → 添加记录。主机记录留空或写 `@` 表示根域名。TTL 可选 600 秒。

## Quick Deploy (Cloudflare Pages)

1. Create a Cloudflare account and **Add Site** (hanlure.com). Change nameservers at 22.cn to the two Cloudflare nameservers shown.
2. In **Pages**, create a new project → **Upload assets** and pick `index.html`.
3. After deploy, bind custom domain:
   - `www` CNAME → `<project>.pages.dev`
   - Apex `@` CNAME → `<project>.pages.dev` (Cloudflare will flatten CNAME automatically).
4. Turn on **Always Use HTTPS** and **Automatic HTTPS Rewrites**.

## Optional
- Replace the mail address in `index.html`: `xu456xu@gmail.com`.
- Add `favicon.ico` at site root (recommended 64×64). Update with `<link rel="icon" href="/favicon.ico">` if you add one.
- Analytics: drop a small script (e.g., Plausible) into `<head>` if needed.
- SEO: keep the provided `<meta>` tags; adjust `description` later.

---

Generated on 2025-10-17.
