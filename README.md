# Robotics Portfolio Static Site

这是适用于 GitHub Pages 的纯静态版本，不需要 React、Vite 或任何构建步骤。

## 文件结构

- `index.html`：主页
- `style.css`：样式
- `assets/`：你自己的图片、视频封面、简历等资源

## 上传到 GitHub Pages

1. 打开你的仓库主页
2. 删除旧的错误版 `index.html`（如果里面是 `export default function ...` 这种 React 源码）
3. 上传本文件夹中的 `index.html` 和 `style.css`
4. 如果需要，再把 `assets/` 目录一起上传
5. 确保 `Settings -> Pages` 中：
   - Source: Deploy from a branch
   - Branch: main
   - Folder: /(root)
6. 等几分钟后刷新站点

## 如何替换视频和图片

### 1. 替换图片占位
你可以把图片放进 `assets/`，然后把 HTML 中类似：

```html
<div class="media-box image-box"></div>
```

改成：

```html
<img class="real-image" src="assets/your_image.jpg" alt="项目图片" />
```

### 2. 替换视频占位
你可以把视频封面图放到 `assets/`，并给卡片链接加上 Bilibili / YouTube / 本地 mp4 链接。

例如：

```html
<a class="media-card" href="https://www.bilibili.com/..." target="_blank">
```

或者用本地 mp4：

```html
<video controls class="real-video">
  <source src="assets/demo.mp4" type="video/mp4" />
</video>
```

## 建议

优先先把网站上线，再逐步替换成真实素材。
