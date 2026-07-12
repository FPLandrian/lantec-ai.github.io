# LanTec AI — official website

The public marketing site for **LanTec AI** and its product **Crewlytics**,
served at **<https://lantec.ai>** via GitHub Pages.

It's a single static page — no build step, no dependencies, no tracking.

```text
.
├── index.html      # the landing page
├── CNAME           # custom domain (lantec.ai)
├── .nojekyll       # serve files as-is
└── assets/         # logo + favicon (PNG)
```

## Preview locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000    # then open http://localhost:8000
# or:  npx serve .
```

## Deploy (GitHub Pages)

1. This repository is public and its contents sit at the repo root.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch →
   `main` / `/ (root)` → Save.**
3. The site goes live within a minute or two.

## Custom domain (lantec.ai)

The `CNAME` file already declares `lantec.ai`, so it appears under
**Settings → Pages → Custom domain**. Add these DNS records at your registrar
(Cloudflare), set to **DNS only** so the certificate can be issued:

| Type  | Name       | Value                    |
| ----- | ---------- | ------------------------ |
| A     | `@` (apex) | `185.199.108.153`        |
| A     | `@` (apex) | `185.199.109.153`        |
| A     | `@` (apex) | `185.199.110.153`        |
| A     | `@` (apex) | `185.199.111.153`        |
| CNAME | `www`      | `<account>.github.io`    |

Once **Settings → Pages → Enforce HTTPS** is available, enable it. Optional IPv6
`AAAA @` records: `2606:50c0:8000::153` … `2606:50c0:8003::153`.

## License

Not open source. © LanTec AI — all rights reserved. The brand assets in
`assets/` are trademarks of LanTec AI.
