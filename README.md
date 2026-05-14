# DroneSys 2026

Source for the workshop website: **DroneSys 2026 — The Second Workshop on Autonomous Drone Computing Systems and Applications**, co-located with ACM/IEEE SEC 2026, Santa Clara, CA.

Live site: <https://dronesys.site/>

## Repository layout

| File | Purpose |
| --- | --- |
| `index.html` | The entire workshop page — content, styling, and layout. |
| `CNAME` | GitHub Pages custom-domain marker (`dronesys.site`). |
| `.nojekyll` | Disables Jekyll processing so files are served as-is. |

## Editing

The site is a single static page with no build step. Edit `index.html` directly — content is in the `<body>`, styling is inline in `<style>` at the top of the file. Push to `main` and GitHub Pages redeploys within a minute.

## Hosting & DNS

Served by **GitHub Pages** from the `main` branch of this repo, on the custom apex domain `dronesys.site`.

DNS records required at the `dronesys.site` registrar (apex domain → A records, not CNAME):

```
A      @      185.199.108.153
A      @      185.199.109.153
A      @      185.199.110.153
A      @      185.199.111.153
AAAA   @      2606:50c0:8000::153
AAAA   @      2606:50c0:8001::153
AAAA   @      2606:50c0:8002::153
AAAA   @      2606:50c0:8003::153
CNAME  www    torreskai0722.github.io
```

After DNS propagates, GitHub auto-issues a Let's Encrypt TLS certificate. Then enable HTTPS enforcement:

```bash
gh api -X PUT repos/Torreskai0722/dronesys/pages -F https_enforced=true
```

Or toggle "Enforce HTTPS" in the repo's Pages settings UI.
