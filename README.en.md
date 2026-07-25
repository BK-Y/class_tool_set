# Cloudflare Static Site

This is a minimal static site template that can be deployed directly to Cloudflare Pages.

## Files

- `index.html`: home page
- `404.html`: 404 page
- `_headers`: response headers
- `_redirects`: 404 fallback rule

## Deploy to GitHub + Cloudflare Pages

1. Push this repository to GitHub.
2. In Cloudflare Pages, choose `Connect to Git`.
3. Select the GitHub repository and the production branch, such as `main`.
4. Use these build settings:

```text
Build command: leave empty
Build output directory: .
```

5. Save and deploy.

After a successful deployment, Cloudflare will provide a `*.pages.dev` URL.

## Local Preview

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
