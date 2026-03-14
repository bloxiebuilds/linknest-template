# 📖 LinkNest — Instructions

Welcome! This guide will get your link-in-bio page live in minutes. No coding experience needed.

---

## 📋 Table of Contents

1. [Getting Started](#1-getting-started)
2. [Editing the Config Block](#2-editing-the-config-block)
3. [Setting Your Theme](#3-setting-your-theme)
4. [Adding & Removing Links](#4-adding--removing-links)
5. [Adding a Profile Photo](#5-adding-a-profile-photo)
6. [Deploying to GitHub Pages](#6-deploying-to-github-pages)
7. [FAQ](#7-faq)

---

## 1. Getting Started

### Option A — Use the Template (Recommended)
1. Go to [github.com/bloxiebuilds/linknest-Link-In-Bio-Template](https://github.com/bloxiebuilds/linknest-Link-In-Bio-Template)
2. Click **"Use this template"**
3. Name your new repo and click **"Create repository"**

### Option B — Clone manually
```bash
git clone https://github.com/bloxiebuilds/linknest-Link-In-Bio-Template.git
```

Open `index.html` in your browser to preview it instantly — no server needed!

---

## 2. Editing the Config Block

Open `index.html` in any text editor. Near the top you will see:

```js
const CONFIG = {
  darkMode:   "toggle",
  customBg:   "#1a1a2e",
  customText: "#eaeaea",

  name:     "Your Name",
  username: "@yourhandle",
  bio:      "Creator. Builder. Dreamer.",
  avatar:   "",

  links: [
    { label: "My Website",  url: "#" },
    ...
  ]
};
```

This is the **only section you need to edit**. Everything else is handled automatically.

| Field | What to put |
|-------|-------------|
| `name` | Your display name |
| `username` | Your handle e.g. `@bloxiebuilds` |
| `bio` | A short one-liner about you |
| `avatar` | A URL to your profile photo, or leave `""` for initials |

---

## 3. Setting Your Theme

Change the `darkMode` value in the config:

| Value | What it does |
|-------|-------------|
| `true` | Always dark mode |
| `false` | Always light mode |
| `"toggle"` | Dark by default, visitor can switch |
| `"custom"` | Uses your own colors (see below) |

### Using a custom color
Set `darkMode` to `"custom"`, then fill in:
```js
customBg:   "#1a1a2e",   // your background color
customText: "#eaeaea",   // your text color
```

Use any hex color code. Tip: find colors at [coolors.co](https://coolors.co).

---

## 4. Adding & Removing Links

In the `links` array, each link looks like this:
```js
{ label: "My Website", url: "https://yoursite.com" },
```

**To add a link** — copy a line and paste it below, then update the label and URL:
```js
{ label: "YouTube", url: "https://youtube.com/@yourchannel" },
```

**To remove a link** — delete the full `{ label: ..., url: ... },` line.

You can add as many links as you want!

---

## 5. Adding a Profile Photo

Set the `avatar` field to a direct image URL:
```js
avatar: "https://yoursite.com/photo.jpg",
```

Or upload your photo to the same folder as `index.html` and reference it like:
```js
avatar: "photo.jpg",
```

If `avatar` is left as `""`, your first initial will show instead.

---

## 6. Deploying to GitHub Pages

1. Push your repo to GitHub (make sure it's **public**)
2. Go to your repo → **Settings** → **Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Click **Save**
5. Your page will be live at:

```
https://YOUR-GITHUB-USERNAME.github.io/linknest-Link-In-Bio-Template
```

---

## 7. FAQ

**Q: Do I need to know how to code?**
No! Just edit the CONFIG block at the top — it's designed to be readable for everyone.

**Q: Can I use this for free?**
Yes — LinkNest is MIT licensed. Free for personal use. Reselling is not permitted.

**Q: Can I add more than 5 links?**
Absolutely — add as many as you like in the `links` array.

**Q: The toggle button isn't showing — why?**
Make sure `darkMode` is set to `"toggle"` (with quotes) in the config.

**Q: Something looks broken — help!**
Make sure every line in the `links` array ends with a comma, and that you haven't accidentally deleted a closing bracket. When in doubt, undo your last change.

---

<p align="center">Made with ❤️ by <a href="https://github.com/bloxiebuilds">bloxiebuilds</a></p>
