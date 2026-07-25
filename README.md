# Class Tool Set · Space4Grow

一个现代化静态测试站点，可用于展示和验证前端页面布局与交互效果。

## 技术栈

- 纯 HTML5 + CSS3
- 无外部依赖
- 响应式设计
- 现代化 UI（渐变 + 毛玻璃效果）

## Cloudflare Pages 部署

本项目已配置为可直接通过 **Cloudflare Pages** 自动部署。

### 部署方式（Git 集成）

1. 将代码推送到 GitHub 仓库：

```bash
git remote add origin https://github.com/你的用户名/class_tool_set.git
git push -u origin main
```

2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
3. 进入 **Pages** 页面，点击 **创建应用程序** > **Pages**
4. 选择 **连接到 Git**，授权 GitHub 并选择本仓库
5. 构建设置如下：

| 配置项 | 值 |
|--------|-----|
| 项目名称 | `inspire`（或自定义） |
| 生产分支 | `main` |
| 构建命令 | 留空（纯静态站点） |
| 部署命令 | `echo "Deployed"`（空操作占位） |
| 构建输出目录 | 留空或填写 `.` |

6. 点击 **保存并部署**，等待部署完成即可

> 💡 **提示**：由于是纯静态站点，无需构建步骤。Cloudflare Pages 会自动识别并部署 `index.html`。

### 项目文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 主页面 |
| `404.html` | 自定义 404 页面 |
| `_headers` | Cloudflare HTTP 头配置 |
| `_redirects` | Cloudflare 重定向规则 |
| `.gitignore` | Git 忽略规则 |

## 本地开发

无需安装，直接用浏览器打开 `index.html` 即可预览：

```bash
# 使用 Python 启动本地服务器
python3 -m http.server 8000
# 访问 http://localhost:8000
```
