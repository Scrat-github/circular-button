# 现代渐变圆形按钮

一个现代风格的圆形按钮组件，采用径向渐变背景，支持 hover 和点击动画效果。

## 效果预览

- **径向渐变背景**：从蓝紫色 `#6366f1` 到紫色 `#8b5cf6`
- **白色图标**：SVG 星形图标
- **Hover 效果**：按钮放大 1.1 倍 + 阴影加深
- **Click 效果**：按压缩小效果
- **响应式设计**：自动适配移动端和桌面端

## 文件结构

```
circular-button/
├── index.html    # 主页面（包含 HTML、CSS 和 JavaScript）
└── README.md     # 使用说明
```

## 快速开始

直接在浏览器中打开 `index.html` 文件即可预览效果。

```bash
# 或使用本地服务器
npx serve .
```

## 自定义配置

通过修改 CSS 变量来快速定制按钮样式：

```css
:root {
  /* 渐变颜色 */
  --gradient-start: #6366f1;  /* 起始颜色 */
  --gradient-end: #8b5cf6;    /* 结束颜色 */

  /* 按钮尺寸 */
  --button-size: 120px;       /* 按钮直径 */
  --icon-size: 48px;          /* 图标大小 */

  /* 阴影效果 */
  --shadow-base: 0 4px 15px rgba(99, 102, 241, 0.4);
  --shadow-hover: 0 8px 30px rgba(99, 102, 241, 0.6);
  --shadow-active: 0 2px 10px rgba(99, 102, 241, 0.3);

  /* 过渡动画 */
  --transition-duration: 0.3s;
  --transition-timing: cubic-bezier(0.4, 0, 0.2, 1);
}
```

## 更换图标

修改 `<svg>` 内的路径即可更换图标。例如，更换为箭头图标：

```html
<svg class="icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 4L10.59 5.41L16.17 11H4V13H16.17L10.59 18.59L12 20L20 12L12 4Z"/>
</svg>
```

## 响应式断点

| 屏幕宽度 | 按钮尺寸 | 图标尺寸 |
|---------|---------|---------|
| > 640px | 120px   | 48px    |
| 380-640px | 100px | 40px    |
| < 380px | 88px    | 36px    |

## 无障碍支持

- 支持键盘 Tab 键聚焦
- `focus-visible` 状态有额外的高亮边框
- `aria-label` 提供屏幕阅读器支持
- 移除移动端点击高亮

## 浏览器兼容性

- Chrome / Edge: ✅ 最新 2 个版本
- Firefox: ✅ 最新 2 个版本
- Safari: ✅ 最新 2 个版本
- iOS Safari: ✅ 12+
- Android Chrome: ✅ 最新 2 个版本

## 许可证

MIT
