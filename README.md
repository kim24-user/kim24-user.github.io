# 金修安个人简历网站

这是一个无需安装依赖、无需构建的纯静态个人简历网站，已经包含：

- 响应式布局（电脑、平板、手机）
- 中文 / 英文切换
- 浅色 / 深色模式
- 页面滚动动画
- 数字验证与数字后端两份 PDF 简历下载
- 打印网页简历
- 基础 SEO、Open Graph、结构化数据
- GitHub Pages / Vercel / Netlify 直接部署

## 1. 本地预览

最简单的方法是直接双击 `index.html`。

更稳定的方式：在本目录打开终端，执行：

```bash
python -m http.server 8000
```

然后浏览器访问：

```text
http://localhost:8000
```

## 2. 修改内容

网站正文集中在 `index.html` 中：

- 姓名、个人介绍、项目、技能、教育背景、联系方式：修改 `index.html`
- 颜色与布局：修改 `assets/css/styles.css`
- 中英文切换、深色模式、动画：修改 `assets/js/main.js`
- 头像：替换 `assets/img/avatar.jpg`
- 两份简历：替换 `assets/docs/` 下对应 PDF，文件名保持不变即可

## 3. GitHub Pages 部署

1. 新建 GitHub 仓库，例如 `resume-site`
2. 将本目录全部文件上传到仓库根目录
3. 打开仓库 `Settings` → `Pages`
4. `Build and deployment` 选择 `Deploy from a branch`
5. 分支选择 `main`，目录选择 `/root`
6. 保存并等待发布完成

若仓库名是 `你的用户名.github.io`，网站地址通常为：

```text
https://你的用户名.github.io/
```

若仓库名是 `resume-site`，网站地址通常为：

```text
https://你的用户名.github.io/resume-site/
```

## 4. Vercel / Netlify 部署

- Vercel：导入该 GitHub 仓库即可，不需要填写构建命令
- Netlify：可直接拖入整个项目文件夹，或连接 GitHub 仓库

## 5. 上线前建议

公开网站会展示手机号和邮箱。若不希望公开手机号，可在 `index.html` 中删除 `tel:` 链接，或改成仅显示邮箱。

`sitemap.xml` 中的域名是占位符，正式上线后请替换成真实网址。
