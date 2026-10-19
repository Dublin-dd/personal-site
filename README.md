# Personal Site · 个人主页

> 一个存放作品、想法与日常观察的个人空间。
> 认真生活，也做些有意思的事情。

纯静态的个人主页，包含 **作品展示 / 随笔记录 / 关于我 / 联系方式** 四个板块，采用手作纸艺风格的视觉设计，响应式布局，适配桌面与移动端。

## ✨ 特性

- 🎨 手作纸艺插画风格，柔和暖色调
- 📱 响应式布局（桌面 / 移动端自适应）
- ♿ 无障碍设计（跳转链接、ARIA 标签、键盘焦点样式）
- ⚡ 纯静态，无任何框架依赖
- 🌙 尊重系统「减少动态效果」偏好

## 📁 目录结构

```
.
├── 个人网站.html              # 单文件版（CSS/JS 内联），可直接浏览器打开
├── dist/                      # 拆分版，用于部署（GitHub Pages 源目录）
│   ├── index.html
│   ├── style.css
│   └── app.js
└── .openai/
    └── hosting.example.json   # OpenAI 托管配置模板
```

> 💡 `个人网站.html` 与 `dist/` 内容一致，前者便于单文件分享，后者便于部署维护。

## 🚀 本地预览

**方式一**：直接用浏览器打开 `个人网站.html`

**方式二**：本地服务器预览 `dist/`

```bash
cd dist
python3 -m http.server 8000
# 然后访问 http://localhost:8000
```

## 🌐 部署

本站通过 **GitHub Pages** 自动部署，源目录为 `dist/`。

访问地址：<https://dublin-dd.github.io/personal-site/>

## ✏️ 如何编辑

- **改文案**：直接编辑 `个人网站.html` 中的文字（如「待补充」占位内容）
- **改样式**：修改 `dist/style.css`（或单文件版内联的 `<style>`）
- **改交互**：修改 `dist/app.js`（作品筛选、弹窗、年份更新等逻辑）

改动后推送到 `main` 分支，GitHub Pages 会自动更新。

## 🔐 注意

`.openai/hosting.json` 含敏感的项目 ID，已加入 `.gitignore`，不会上传。如需配置 OpenAI 托管，请参考 `.openai/hosting.example.json` 自行创建。
