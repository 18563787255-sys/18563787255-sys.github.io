# Fiona · 张云涵的个人主页

中英文双语、六个切页、杂志拼贴风。纯静态网站，无需安装依赖或运行构建。

## 本地查看

双击 `index.html` 即可。请保留整个文件夹，图片依赖 `assets` 目录。

## 上传 GitHub Pages

1. 在 GitHub 新建仓库，例如 `fiona-portfolio`。
2. 将本文件夹**里面的文件**上传到仓库根目录：确保根目录直接有 `index.html`，而不是再套一层 `fiona-github`。
3. 打开仓库 **Settings → Pages**。在 **Build and deployment** 下选择 **Deploy from a branch**，分支选择 **main**，目录选择 **/(root)**，保存。
4. 等待 Pages 部署完成。网站地址一般为 `https://你的用户名.github.io/fiona-portfolio/`，以 Pages 设置页显示的链接为准。

如果希望使用已附带的自动发布流程，可在第3步把 Source 选择为 **GitHub Actions**，并确保 `.github/workflows/pages.yml` 也已上传。两种方式选一种即可。默认流程使用 `main` 分支。

## 文件说明

- `index.html`：网页入口。
- `styles.css`：配色、杂志排版、移动端适配。
- `content.js`：五个内容板块的中英文文字；修改这里可更新简历内容。
- `app.js`：首页内容、语言切换和页面导航。
- `assets/`：首页背景与六张个人照片。
- `.nojekyll`：静态资源配置。
- `.github/workflows/pages.yml`：可选 GitHub Pages 自动发布流程。

## 修改图片与内容

首页背景为 `assets/love-yourself.jpg`。首页两张照片分别为 `gallery.jpg`（绿色外套，总第10张）与 `night.jpg`（夜晚灰色上衣，总第7张）。其他照片用于内页拼贴。前四张参考图仅用于设计参考，没有直接嵌入网站。

在 `content.js` 中，每段文字包含 `zh` 与 `en`。同步修改两种语言即可。切换语言后会保留当前页面，并记住当前浏览器的语言偏好。

所有页面采用相对资源路径和 hash 导航，可部署到 GitHub Pages 仓库子路径，不需要服务器路由设置。

内容依据提供的简历整理，保留“欧莱雅 Brainstorm”原文写法。若正式赛事名称需更正，可在 `content.js` 内同步更新。网页未加入电话号码、邮箱或原始简历下载文件。

GitHub 官方发布说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

