# 🐦‍⬛ Raven Store

A landing page for a Discord bots & services store, built as a **single file** — no build step, no dependencies to install.

<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Lucide%20Icons-000000?style=for-the-badge&logo=lucide&logoColor=white" alt="Lucide Icons">
</p>

<p>
  <img src="https://img.shields.io/badge/Single%20File-100%25-success?style=flat-square" alt="Single File">
  <img src="https://img.shields.io/badge/RTL-Supported-blue?style=flat-square" alt="RTL">
  <img src="https://img.shields.io/badge/License-Custom-lightgrey?style=flat-square" alt="License">
</p>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#️-tech-stack)
- [How to Open the Site](#-how-to-open-the-site)
- [⚙️ Customizing Your Server Name & Logo (Important)](#️-customizing-your-server-name--logo)
- [Site Sections](#-site-sections)
- [FAQ](#-faq)

---

## 🔍 Overview

This project is a **single HTML file** (`raven-store.html`) that contains everything:
markup, styling (CSS), and interactivity (JavaScript) — no extra folders, no build tools (no npm/build step needed). Just open the file directly in a browser, or upload it to any hosting service.

## ✨ Features

- 🎨 Professional dark theme with red gradients. The visible page content is in Arabic (RTL), but the code and comments are easy to read and edit.
- 📱 Fully responsive across mobile, tablet, and desktop.
- ⚡ Animated loading screen with a progress bar.
- 🧩 All sections (features, services, reviews, FAQ) are generated dynamically from JavaScript arrays — add or remove an item by editing a single line.
- ❓ Collapsible FAQ accordion section.
- 🔗 One single place to control the server name, logo, and Discord invite link (instead of hunting through the whole code).

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5** | Page structure |
| **CSS3** (hand-written, no frameworks) | All styling, effects, and animations |
| **JavaScript (Vanilla JS)** | Content generation, loading screen, mobile menu, FAQ accordion |
| **[Lucide Icons](https://lucide.dev)** | Icons (loaded via CDN) |
| **[Google Fonts – Cairo](https://fonts.google.com/specimen/Cairo)** | Arabic font |

> No installation (`npm install`) or build step required — everything runs from a single file.

## 🚀 How to Open the Site

1. Download the `raven-store.html` file.
2. Double-click it to open directly in your browser, or upload it to any static hosting service (Netlify, Vercel, GitHub Pages, or regular web hosting) and it will work immediately.

## ⚙️ Customizing Your Server Name & Logo

All of your server's data (name, logo, Discord link) lives in **one single place** inside the file, so it's easy to find:

1. Open `raven-store.html` in any code editor (e.g. [VS Code](https://code.visualstudio.com/)).
2. Press `Ctrl + F` (or `Cmd + F` on Mac) and search for: `SITE_CONFIG`
3. It will take you straight to this block (near the end of the file):

```javascript
const SITE_CONFIG = {
  serverName: "RAVEN",                       // ← your server/store name
  logoUrl: "",                                // ← your server logo image URL
  discordUrl: "https://discord.gg/r-ns"       // ← your Discord invite link
};
```

| Field | What to put here |
|---|---|
| `serverName` | Your store/server name, e.g. `"Raven Store"` — it will automatically appear everywhere on the page (navbar, loading screen, footer). |
| `logoUrl` | A direct link to your logo image (ending in `.png`, `.webp`, or `.jpg`). Upload the image to any image host (e.g. [imgur](https://imgur.com) or Discord's CDN) and paste the direct link here. If left empty `""`, the first letter of your server name will be shown automatically instead of an image. |
| `discordUrl` | Your actual Discord server invite link, e.g. `"https://discord.gg/xxxxxxx"`. |

Once you update these three values and save the file, the name, logo, and link will automatically update **everywhere on the page** — no need to search through the code or repeat the change.

> ⚠️ **Note:** The exact line number may shift slightly depending on your editor or if you've made other edits to the file, so it's best to rely on searching for `SITE_CONFIG` rather than a fixed line number.

## 📑 Site Sections

| Section | Description |
|---|---|
| Hero | Main headline and Discord join button |
| About | Store overview and stats (years of experience, clients, bots built...) |
| Features | 6 cards highlighting why customers should choose you |
| Services | Services offered (bots, designs, hosting...) |
| How We Work | 4-step process explaining how you work with clients |
| Reviews | Customer testimonials and ratings |
| FAQ | Collapsible frequently asked questions |
| Footer | Quick links and copyright |

## ❓ FAQ

**Q: Can I add/remove a service, FAQ item, or review?**
Yes — each of these sections is built from a JavaScript array near the top of the `<script>` section, such as `services`, `faqs`, or `reviews`. Copy the format of an existing item, change the text, and it will automatically appear on the page.

**Q: Does the site work offline?**
It needs an internet connection only to load the font and icons from CDN links; the rest of the site runs from the same file.

**Q: How do I change the red color scheme to something else?**
Search the file for `#dc2626`, `#ef4444`, and `#b91c1c` (the red shades used) and replace them with your preferred color.

---
