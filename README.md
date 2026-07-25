# Cloudflare Worker Static Site

这是一个最小可用的 Cloudflare Worker 项目，用 Worker 直接托管仓库中的静态文件。

## 文件结构

- `public/index.html`：首页
- `public/404.html`：404 页面
- `_headers`：响应头配置
- `_redirects`：静态资源回退规则
- `wrangler.toml`：Worker 配置
- `src/index.js`：Worker 入口

## Cloudflare Worker 部署

如果你在 Cloudflare 后台看到的是“创建 Worker”而不是“创建 Pages”，就按下面方式部署：

1. 仓库推送到 GitHub，或者由 Gitee 镜像同步到 GitHub。
2. 在 Cloudflare 的 Worker 创建页选择这个仓库。
3. 使用下面配置：

```text
构建命令: 留空
部署命令: npx wrangler deploy
```

4. Cloudflare 会读取 `wrangler.toml`，并把 `public` 目录中的静态资源通过 Worker 发布出去。

## 部署原理

`src/index.js` 会把所有请求转发到 `ASSETS` 绑定的静态目录。
当请求的文件不存在时，会返回 `public/404.html`。
