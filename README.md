# 金修安个人简历网站（GitHub Pages 修正版）

本版本已经修复：

- CSS 未加载导致页面像纯文字的问题
- 头像路径失效的问题
- GitHub Pages 子目录下简历下载失败的问题
- 上传 assets 文件夹不完整导致的资源 404 问题

## 最稳妥的上传方式

仓库根目录只需要看到以下文件：

```text
index.html
404.html
resume-verification.pdf
resume-physical-design.pdf
.nojekyll
```

其中 `index.html` 已内嵌 CSS、JavaScript、头像，以及两份 PDF 的下载回退数据。即使 PDF 文件漏传，网页按钮仍可以下载内嵌简历；保留两个 PDF 文件是为了兼容直接访问和搜索引擎。

## 更新 GitHub 仓库

1. 打开仓库主页。
2. 删除旧的 `index.html`、`404.html`，以及旧的 `assets` 文件夹（可选但建议）。
3. 点击 **Add file → Upload files**。
4. 将本目录内的五个文件全部拖入上传区。不要上传 ZIP，也不要再套一层文件夹。
5. 点击 **Commit changes**。
6. 等待 GitHub Pages 重新部署，然后按 `Ctrl + F5` 强制刷新。

## 判断是否上传正确

打开仓库主页时，文件列表最外层应直接显示 `index.html`，而不是先显示一个 `jin-xiuan-resume-site-fixed` 文件夹。

## 本地预览

在本目录打开终端：

```powershell
python -m http.server 8000
```

浏览器访问：

```text
http://127.0.0.1:8000
```
