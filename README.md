# anupabhattacharyya.com

Personal profile website — a single-page static site (HTML/CSS/JS, no build step, no framework).

## Structure

```
.
├── index.html     # All page content
├── styles.css     # Styling (dark, responsive portfolio theme)
├── script.js      # Nav, scroll animations, count-up stats, typing headline
└── CNAME          # Custom domain for GitHub Pages
```

## Run locally

Just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this repo to GitHub (public).
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Under **Custom domain**, enter `www.anupabhattacharyya.com` (matches the `CNAME` file).
4. At your domain registrar, add DNS records:
   - `CNAME` record: `www` → `<your-github-username>.github.io`
   - Four `A` records for the apex domain `anupabhattacharyya.com` pointing to GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
5. Enable **Enforce HTTPS** in Pages settings once the certificate is issued.

## License

MIT — see [LICENSE](LICENSE).
