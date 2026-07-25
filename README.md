# Cloudflare Static Site

这是一个最小可用的静态站点模板，适合直接部署到 Cloudflare Pages。

## 文件结构

- `index.html`：首页
- `404.html`：404 页面
- `_headers`：响应头配置
- `_redirects`：404 回退规则

## 部署到 GitHub + Cloudflare Pages

1. 把仓库推送到 GitHub。
2. 在 Cloudflare Pages 中选择 `Connect to Git`。
3. 绑定 GitHub 仓库，并选择生产分支，例如 `main`。
4. 构建设置使用下面这组值：

```text
Build command: 留空
Build output directory: .
```

5. 保存并部署。

部署成功后，Cloudflare 会提供一个 `*.pages.dev` 域名用于访问。

## 本地预览

```bash
python3 -m http.server 8000
```

然后访问 `http://localhost:8000`。
