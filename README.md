# HTTP Status Code Lookup Tool

> A handy developer tool to quickly browse, filter, and search HTTP status codes with detailed explanations.

[📖 中文文档](./README-zh.md)

## ✨ Features

- **Complete Status Code List** – covers 1xx, 2xx, 3xx, 4xx, and 5xx codes with typical usage scenarios.
- **Category Filtering** – filter by informational, success, redirection, client error, or server error.
- **Live Search** – search by status code number, title, or description.
- **Expandable Details** – click any card to see a detailed explanation and real‑world context.
- **100% Local** – runs entirely in your browser; no backend, no data upload.
- **Clean UI** – modern, responsive design with SVG icons (no emoji).

## 🚀 How to Use

1. Download the three files (`index.html`, `style.css`, `script.js`) into the same folder.
2. Open `index.html` with any modern web browser.
3. Or deploy the folder to GitHub Pages, Netlify, or any static hosting service.

### Quick Start with GitHub Pages

- Push the files to a GitHub repository.
- Enable **GitHub Pages** in the repository settings (branch `main`, root folder).
- Your tool will be available at `https://<your-username>.github.io/<repo-name>/`

## 🎨 Customisation

### Add / Modify Status Codes

Edit the `statusData` array in `script.js`. Each entry has:

```javascript
{
  code: 418,
  category: "clientError",
  title: "I'm a teapot",
  description: "The server refuses to brew coffee because it is a teapot.",
  details: "An April Fools’ joke from 1998, defined in RFC 2324."
}
```

Available `category` values: `"info"`, `"success"`, `"redirect"`, `"clientError"`, `"serverError"`.

### Change Icons

All icons are stored as inline SVG strings inside the `svgIcons` object in `script.js`. You can replace any icon with your own SVG code.

```javascript
const svgIcons = {
  header: '<svg>...</svg>',
  categoryInfo: '<svg>...</svg>',
  // ...
};
```

You can also get an array of all SVG strings using `Object.values(svgIcons)`.

### Adjust Styling

Open `style.css` and modify CSS variables (colors, border radius, shadows, etc.) to match your preference.

## 📦 Dependencies

None – pure HTML/CSS/JavaScript. Works offline after first load.

## 🤝 Contributing

Feel free to open an issue or submit a pull request if you have ideas to improve this tool.

## 📄 License

MIT – use it anywhere, for any purpose.
