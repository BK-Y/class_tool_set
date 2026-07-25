# Class Tool Set · Space4Grow

A modern static testing site for demonstrating and verifying frontend page layouts and interactions.

## Tech Stack

- Pure HTML5 + CSS3
- Zero external dependencies
- Responsive design
- Modern UI (gradients + glassmorphism effects)

## Cloudflare Pages Deployment

This project is configured for automatic deployment via **Cloudflare Pages**.

### Deploy with Git Integration

1. Push the code to a GitHub repository:

```bash
git remote add origin https://github.com/your-username/class_tool_set.git
git push -u origin main
```

2. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/)
3. Go to **Pages** > **Create application** > **Pages**
4. Click **Connect to Git**, authorize GitHub, and select this repository
5. Build settings:

| Setting | Value |
|---------|-------|
| Project name | `class-tool-set` (or custom) |
| Production branch | `main` |
| Build command | Leave empty (static site) |
| Build output directory | Leave empty or set to `.` |

6. Click **Save and Deploy** and wait for completion

> 💡 **Tip**: Since this is a pure static site, no build step is required. Cloudflare Pages will automatically detect and deploy `index.html`.

### Project Files

| File | Description |
|------|-------------|
| `index.html` | Main page |
| `404.html` | Custom 404 page |
| `_headers` | Cloudflare HTTP headers configuration |
| `_redirects` | Cloudflare redirect rules |
| `wrangler.toml` | Cloudflare Workers/Pages config |
| `.gitignore` | Git ignore rules |

## Local Development

No installation needed — just open `index.html` in your browser:

```bash
# Start a local server with Python
python3 -m http.server 8000
# Visit http://localhost:8000
```
