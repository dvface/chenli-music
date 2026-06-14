# ✨ 陈粒 · 星云音乐站

一个 Apple Music 风格的交互式音乐页面，致敬独立音乐人陈粒。  
包含 32 首热门歌曲、动态星云粒子背景、可展开的歌曲星云系统。

> 🎁 送给小周

---

## 🚀 快速部署（GitHub Pages — 免费，3 分钟）

### 第一步：注册 GitHub

1. 打开 https://github.com 注册账号
2. 验证邮箱

### 第二步：创建仓库

1. 点击右上角 **+** → **New repository**
2. Repository name 填写：`chenli-music`（或任意名称）
3. 选择 **Public**
4. 点击 **Create repository**

### 第三步：上传文件

**方法 A — 网页拖拽上传（最简单）：**
1. 在仓库页面点击 **uploading an existing file**
2. 把本项目所有文件拖进去：
   - `index.html`
   - `audio/` 文件夹（含你的 MP3 文件）
3. 点击 **Commit changes**

**方法 B — 命令行（推荐，方便后续更新）：**
```bash
git clone https://github.com/你的用户名/chenli-music.git
cd chenli-music
# 把 index.html 和 audio/ 文件夹复制到这里
git add .
git commit -m "初始化陈粒星云音乐站"
git push origin main
```

### 第四步：开启 Pages

1. 仓库页面 → **Settings** → 左侧 **Pages**
2. **Branch** 选择 `main`，**Save**
3. 等待 30 秒，页面自动部署
4. 获得链接：`https://你的用户名.github.io/chenli-music/`

### 第五步（可选）：绑定自定义域名

1. 在 Pages 设置中 **Custom domain** 填入你的域名
2. 到域名 DNS 添加 CNAME 记录指向 `你的用户名.github.io`
3. 勾选 **Enforce HTTPS**

---

## 📁 项目结构

```
chenli-music/
├── index.html          ← 主页面（单文件包含所有 CSS/JS）
├── audio/
│   ├── README.md       ← 音频文件说明
│   └── *.mp3           ← 32 首歌曲 MP3（需自行准备）
└── README.md           ← 本文件
```

---

## 🎵 准备音频文件

详见 `audio/README.md`。

你需要将 32 首陈粒歌曲的 MP3 文件放入 `audio/` 文件夹，文件名必须与代码中定义的一致。

**没有 MP3 文件也能运行！**  
页面在无音频文件时仍可正常展示星云动画和所有交互，只是播放音乐会提示"找不到文件"。

---

## 💻 本地运行

直接双击 `index.html` 在浏览器中打开即可。

---

## ⌨️ 快捷键

| 按键 | 功能 |
|------|------|
| 空格 | 播放 / 暂停 |
| ← → | 上一首 / 下一首 |
| ↑ ↓ | 音量增减 |
| M | 静音 / 取消静音 |
| 点击中央星星 | 展开 / 收缩歌曲星云 |
| 点击小星星 | 播放对应歌曲 |
| 点击右上角 ☰ | 打开歌曲列表 |

---

## 📱 兼容性

- ✅ Chrome / Edge / Safari / Firefox
- ✅ iOS Safari（支持安全区域）
- ✅ Android Chrome
- ✅ 桌面端 & 移动端全适配

---

## 🎨 特性

- 🌌 Canvas 动态星云粒子系统（200 颗粒子 + 4 层星云雾气）
- ⭐ 32 颗歌曲星星，3 条黄金螺旋臂布局
- 🎧 Apple Music 风格播放器（磨砂玻璃、进度拖拽）
- 📋 歌曲列表面板（底部滑出式 Sheet）
- ✨ 纯 CSS 动画（旋转、呼吸、跳动），GPU 加速
- 🌙 深色星云主题，SF Pro 字体优先
- ♿ 键盘无障碍操作

---

## ⚠️ 注意事项

- **音频文件不上传 GitHub**：建议将 `audio/` 加入 `.gitignore`，MP3 文件通过其他方式（OSS/CDN）托管。GitHub 仓库有 1GB 限制。
- 如果 GitHub Pages 访问慢，可改用 **Vercel** 或 **Cloudflare Pages** 部署（步骤类似）。
- 如需云端托管 MP3 文件，推荐 **Cloudflare R2**（10GB 免费）或 **阿里云 OSS**。
