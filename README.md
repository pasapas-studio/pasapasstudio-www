# pasapas.studio

Static site for Pas à Pas Studio LLC. Single `index.html`, no build step. Hosted on GitHub Pages.

## Deploy

1. Push this repo to GitHub.
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Custom domain: `pasapas.studio` (already set via `CNAME` file). Tick **Enforce HTTPS** once the cert is issued.

## DNS (at the domain registrar)

| Type  | Host | Value                   |
|-------|------|-------------------------|
| A     | @    | 185.199.108.153         |
| A     | @    | 185.199.109.153         |
| A     | @    | 185.199.110.153         |
| A     | @    | 185.199.111.153         |
| AAAA  | @    | 2606:50c0:8000::153     |
| AAAA  | @    | 2606:50c0:8001::153     |
| AAAA  | @    | 2606:50c0:8002::153     |
| AAAA  | @    | 2606:50c0:8003::153     |
| CNAME | www  | `<github-username>.github.io` |

Recommended: verify the domain in GitHub (Settings → Pages → Verified domains) to prevent takeover.

## Local preview

    python3 -m http.server 8000
