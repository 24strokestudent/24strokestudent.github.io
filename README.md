# 24strokestudent 的个人主页

基于 [Hugo](https://gohugo.io/) 构建的静态站点，内容以学习笔记、项目记录为主。

## 主题与许可

- 主题：[hugo-theme-reimu](https://github.com/D-Sketon/hugo-theme-reimu)
- 许可证：MIT License · Copyright (c) 2024 D-Sketon
- 许可证全文见 [`themes/reimu/LICENSE`](themes/reimu/LICENSE)

主题按 MIT 协议使用：允许修改、分发与商用，保留上述版权声明即可。

## 本地预览

```bash
hugo server -D
# 打开 http://localhost:1313
```

## 构建

```bash
hugo --baseURL https://your-domain/ --destination public
```

> `baseURL` 必须和实际访问地址一致，否则 CSS、图片和分享链接会指向错误的主机。

## 部署

推送到 `main` 分支后，由 GitHub Actions（`.github/workflows/hugo.yaml`）自动完成：

1. **Cloudflare Pages**（主站）：构建后通过 `wrangler pages deploy` 发布，绑定 `24strokestudent.tech`，全球 CDN + 自动 HTTPS；
2. **自建服务器**（备用）：`rsync` 到阿里云服务器，用 IP 访问。

> 为什么不用国内服务器绑域名：大陆节点需要 ICP 备案，所以主站放在 Cloudflare Pages。

## 内容说明

- `content/`：文章与页面
- `static/`：图片等静态资源
- `data/vendor.yml`：前端依赖（已全部本地化，不依赖第三方 CDN）
