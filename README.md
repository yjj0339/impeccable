# Impeccable 落地页

**线上地址：https://yjj0339.github.io/impeccable/**

前端设计工具集 Impeccable 的产品发布落地页，浅色「未来玻璃」风格，对标 Apple 发布会的克制气质。

## 技术要点

- 单 HTML 文件交付，原生 CSS/JS，零框架、零 CDN、零外部字体
- 图标全部为硬编码 Lucide 风格内联 SVG，无 Emoji
- 浅色为默认主题，可一键切换深靛蓝宇宙版，`localStorage` 记忆偏好，初始值遵守 `prefers-color-scheme`
- 动画仅用 transform/opacity，入场由 IntersectionObserver 在 20% 视口处触发
- `prefers-reduced-motion` 下所有动画压缩为 0.01ms，3D 透视拍平，轮播停止自动播放
- 颜色、圆角、阴影全部走 CSS 令牌，无令牌外裸色值

## 页面结构

固定毛玻璃导航 → Hero（胶囊标签 + 渐变大标题 + 双 CTA + CSS 3D 玻璃平板 mockup）→ 3×3 特性网格 → 评价轮播（4s 自动播放 + 拖拽切换）→ FAQ 折叠 → 邮箱订阅（loading + toast）→ 页脚

## 本地预览

```bash
node tools/server.js
```

终端会打印局域网地址，手机与电脑连同一 WiFi 即可扫码或输入地址访问。

## 部署

GitHub Pages，仓库根目录发布，`main` 分支。
