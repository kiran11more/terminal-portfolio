# Kiran More — Interactive Terminal Portfolio

> Lightweight, zero-dependency interactive terminal portfolio designed to deploy on Cloudflare Pages at [cli.kiranm.in](https://cli.kiranm.in).

[![Live CLI Demo](https://img.shields.io/badge/Demo-cli.kiranm.in-amber?style=flat-square&logo=gnometerminal)](https://cli.kiranm.in)
[![Main Portfolio](https://img.shields.io/badge/Main%20Site-kiranm.in-blue?style=flat-square)](https://kiranm.in)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

An authentic macOS-style terminal emulator built entirely with semantic HTML5, modern CSS custom properties, and vanilla JavaScript. Visitors can explore technical skills, past case studies, switch between light and dark themes, and chat with a live AI assistant powered by Cloudflare Workers AI.

---

## ⚡ Highlights & Features

- **Zero Dependencies:** Single self-contained `index.html` with zero build tools, node modules, or npm scripts required.
- **macOS Window Chrome:** Centered 960px card with authentic traffic-light controls (close, reset, theme toggle) and a custom titlebar (`kiran@terminal: ~`).
- **Dynamic Themes:**
  - **Light Mode (Default):** Clean `#f5f5f5` terminal surface, `#e9ecef` backdrop, `#e67e22` user prompt, and `#008080` host prompt.
  - **Dark Mode:** High-contrast `#161b22` surface, `#f39c12` user prompt, and `#2dd4bf` host prompt.
  - Switches via `theme [light|dark]` or the titlebar toggle, persisted in `localStorage`.
- **Live Workers AI Integration (`ai <question>`):** Directly queries the live Cloudflare Pages Function at `https://kiranm.in/api/chat` with real-time thinking states and safe link formatting.
- **Authentic Terminal UX:**
  - `ArrowUp` / `ArrowDown` command history navigation.
  - `Tab` command autocompletion with inline suggestions.
  - `Ctrl + L` screen clearing.
  - Auto-focus input on terminal click (without hijacking user text selection).
  - Strict HTML escaping for user inputs to prevent XSS.
  - Responsive design optimized for mobile touchscreens (`@media (max-width: 640px)`).

---

## ⌨️ Available Commands

| Command | Description |
| :--- | :--- |
| `welcome` | Re-renders the slanted ASCII emblem and profile introduction |
| `help` | Lists all available terminal commands and syntax |
| `about` | Summary of 10+ years engineering background, philosophy, and client collaboration |
| `stack` | Complete breakdown of CMS, E-commerce, modern frontend, edge, and SEO tooling |
| `work` | Featured client projects, live case studies, and trade demo landers |
| `ai <question>` | Real-time AI consultation powered by Cloudflare Workers AI (`@cf/meta/llama-3.1-8b-instruct-fp8-fast`) |
| `theme [light\|dark]` | Switch or toggle between light and dark terminal palettes |
| `gui` | Opens the graphical visual portfolio ([https://kiranm.in](https://kiranm.in)) in a new browser tab |
| `contact` | Direct contact channels (`hello@kiranm.in`), GitHub, and location |
| `clear` | Clears terminal scrollback history (or shortcut `Ctrl+L`) |

---

## 🚀 Cloudflare Pages Deployment

This project requires **zero build step** and can be deployed in seconds on Cloudflare Pages:

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "feat: initial commit for interactive terminal portfolio"
   git branch -M main
   git remote add origin https://github.com/kiran11more/terminal-portfolio.git
   git push -u origin main
   ```

2. **Connect to Cloudflare Pages:**
   - Log into the [Cloudflare Dashboard](https://dash.cloudflare.com/) &rarr; **Workers & Pages** &rarr; **Create application** &rarr; **Pages** &rarr; **Connect to Git**.
   - Select repository: `kiran11more/terminal-portfolio`.
   - **Framework preset:** `None`.
   - **Build command:** *(leave empty)*.
   - **Build output directory:** `.` *(root)*.
   - Click **Save and Deploy**.

3. **Custom Domain:**
   - In your Pages project settings, go to **Custom domains** &rarr; **Set up a custom domain**.
   - Enter `cli.kiranm.in` and follow Cloudflare's automatic DNS configuration.

---

## 🛠️ Local Development & Testing

Run any lightweight static server:

```bash
# Python
python -m http.server 8080

# Node / npx
npx serve .

# PHP
php -S localhost:8080
```

Open `http://localhost:8080` in your browser.

---

## 📄 License

MIT &copy; [Kiran More](https://kiranm.in)
