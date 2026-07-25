# Cloudflare Worker Static Site

This is a minimal Cloudflare Worker project that serves the repository's static files through a Worker.

## Files

- `index.html`: home page
- `404.html`: 404 page
- `_headers`: response headers
- `_redirects`: fallback rule
- `wrangler.toml`: Worker configuration
- `src/index.js`: Worker entrypoint

## Deploy as a Cloudflare Worker

If the Cloudflare UI shows "Create Worker" instead of Pages, deploy it with this setup:

1. Push the repository to GitHub, or mirror it from Gitee to GitHub.
2. Select the repository in the Cloudflare Worker creation flow.
3. Use these settings:

```text
Build command: leave empty
Deploy command: npx wrangler deploy
```

4. Cloudflare will read `wrangler.toml` and publish the static files through the Worker.

## How it works

`src/index.js` forwards every request to the `ASSETS` binding.
If the requested file does not exist, it returns `404.html`.
