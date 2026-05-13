# DroneSys 2026

Source for the workshop website: **DroneSys 2026 — The Second Workshop on Autonomous Drone Computing Systems and Applications**, co-located with ACM/IEEE SEC 2026, Santa Clara, CA.

## Editing

The site is a single static page. Edit `index.html` directly; styling is inline in `<style>` at the top of the file.

## Deployment

Served via GitHub Pages from the `main` branch.

- Project page URL: `https://torreskai0722.github.io/dronesys/`
- Linked from: [liangkai.org/dronesys/](https://liangkai.org/dronesys/)

To enable Pages after creation:

```bash
gh api -X POST repos/Torreskai0722/dronesys/pages -f source[branch]=main -f source[path]=/
```

## Custom subdomain (optional)

To serve at `dronesys.liangkai.org`:

1. Add a `CNAME` file with `dronesys.liangkai.org` in this repo.
2. Add a DNS `CNAME` record `dronesys` → `torreskai0722.github.io` in the liangkai.org DNS console.
