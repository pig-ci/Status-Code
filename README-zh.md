# HTTP 状态码速查工具

> 一款面向开发者的实用小工具，支持分类浏览、关键词搜索 HTTP 状态码，并附带详细场景说明。

## ✨ 功能特性

- **完整的状态码列表** – 涵盖 1xx、2xx、3xx、4xx、5xx 常见状态码及典型使用场景。
- **分类过滤** – 按信息、成功、重定向、客户端错误、服务端错误快速筛选。
- **实时搜索** – 支持按状态码数字、标题或描述进行关键词查找。
- **展开详情** – 点击任意卡片可查看更详细的技术说明与实际应用场景。
- **完全本地运行** – 纯前端实现，所有数据均在前端存储，不会上传任何内容。
- **简洁现代的界面** – 响应式设计，使用 SVG 图标（无 Emoji），美观且轻量。

## 🚀 使用方法

1. 将三个文件（`index.html`、`style.css`、`script.js`）下载到同一个文件夹中。
2. 用任意现代浏览器打开 `index.html` 即可使用。
3. 或者将整个文件夹部署到 GitHub Pages、Netlify 或其他静态托管服务。

### 通过 GitHub Pages 快速部署

- 将文件推送到 GitHub 仓库。
- 在仓库设置中启用 **GitHub Pages**（分支选择 `main`，目录为根目录）。
- 通过 `https://<你的用户名>.github.io/<仓库名>/` 访问工具。

## 🧰 文件结构

```
.
├── index.html      # 页面结构
├── style.css       # 样式（响应式布局）
└── script.js       # 逻辑、数据以及 SVG 图标数组
```

## 🎨 自定义修改

### 增加或修改状态码

编辑 `script.js` 中的 `statusData` 数组。每个条目结构如下：

```javascript
{
  code: 418,
  category: "clientError",
  title: "I'm a teapot",
  description: "服务器拒绝煮咖啡，因为它是一个茶壶。",
  details: "1998 年的愚人节玩笑，定义在 RFC 2324 中。"
}
```

可用的 `category` 值：`"info"`、`"success"`、`"redirect"`、`"clientError"`、`"serverError"`。

### 更换图标

所有图标均以内联 SVG 字符串的形式存储在 `script.js` 的 `svgIcons` 对象中。你可以用自己设计的 SVG 代码替换任意图标。

```javascript
const svgIcons = {
  header: '<svg>...</svg>',
  categoryInfo: '<svg>...</svg>',
  // ...
};
```

如果需要获得所有 SVG 字符串组成的数组，可使用 `Object.values(svgIcons)`。

### 调整样式

打开 `style.css`，修改 CSS 变量（颜色、圆角、阴影等）以满足个性化需求。

## 📦 依赖

无任何外部依赖 —— 纯 HTML/CSS/JavaScript。首次加载后即可离线使用。

## 🤝 参与贡献

如果你有改进建议，欢迎提交 Issue 或 Pull Request。

## 📄 许可证

MIT – 可任意使用，包括商业用途。
