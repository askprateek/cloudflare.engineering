# cloudflare.engineering

Source for the cloudflare.engineering contact page, served by GitHub Pages.

## GitHub Pages setup

Repo **Settings → Pages**:

1. Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
2. Custom domain: `cloudflare.engineering` (also set by the `CNAME` file).
3. After the certificate is issued, enable **Enforce HTTPS**.

## DNS (Cloudflare)

Apex `cloudflare.engineering`, either:

- four `A` records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, or
- one `CNAME` `@` → `askprateek.github.io` (Cloudflare flattens it at the apex).

Keep the Cloudflare proxy **off (DNS only, grey cloud)** until GitHub has issued the certificate; then enable Enforce HTTPS. If you turn the proxy on later, set SSL/TLS mode to **Full (strict)**.
