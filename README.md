# 🌐 GitHub HTML Viewer

> Instantly preview any GitHub-hosted `.html` file — no cloning, no local server.

[![Star on GitHub](https://img.shields.io/github/stars/ghviz/github-html-viewer?style=social)](https://github.com/ghviz/github-html-viewer)

---

## 🔍 What is this?

**GitHub HTML Viewer** is a lightweight, zero-dependency tool that lets you paste any GitHub `.html` blob URL and renders it live in your browser — right inside the page.

GitHub shows raw HTML source by default. This tool fixes that.

---

## 🚀 Demo

🔗 **[Try it live →](https://ghviz.github.io/github-html-viewer)**

**Example input:**
```
https://github.com/shanraisshan/claude-code-best-practice/blob/main/presentation/index.html
```

**Output:** Fully rendered HTML page, previewed instantly.

---

## ✨ Features

- ✅ Paste any `github.com/.../blob/.../file.html` URL
- ✅ Renders HTML live via sandboxed iframe
- ✅ Uses **GitHub Contents API** — no CORS issues
- ✅ Zero dependencies — single `.html` file
- ✅ Press `Enter` or click **Render ▶** to load
- ✅ Shows file size & fetch status

---

## 🛠 How It Works

1. Parses the GitHub blob URL to extract `owner`, `repo`, `branch`, and `path`
2. Fetches the file content via the **GitHub Contents API** (`api.github.com/repos/...`)
3. Decodes the base64 response
4. Injects the HTML into a sandboxed `<iframe>` using `srcdoc`

```
GitHub Blob URL
     ↓
GitHub Contents API (CORS-friendly)
     ↓
Base64 decode
     ↓
<iframe srcdoc="..."> → Live Preview
```

---

## 📦 Usage

No install needed. Just open `index.html` in any browser — or use the hosted version.

```bash
git clone https://github.com/ghviz/github-html-viewer.git
cd github-html-viewer
open index.html
```

---

## ⚠️ Limitations

| Limitation | Detail |
|---|---|
| API rate limit | 60 requests/hour (unauthenticated) |
| Private repos | Not supported without a GitHub token |
| Relative assets | Images/CSS using relative paths may not load |
| Non-HTML files | Only `.html` files are supported |

---

## 🤝 Contributing

PRs and issues are welcome! If you find a bug or have a feature idea, [open an issue](https://github.com/ghviz/github-html-viewer/issues).

---

## 📄 License

MIT © [ghviz](https://github.com/ghviz)
