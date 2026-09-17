# GameSense Discord Theme (Fixed & Modernized)

[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![BetterDiscord](https://img.shields.io/badge/BetterDiscord-Compatible-202225?style=for-the-badge&logo=discord&logoColor=5865F2)](https://betterdiscord.app/)
[![Vencord](https://img.shields.io/badge/Vencord-Compatible-333333?style=for-the-badge&logo=discord&logoColor=57F287)](https://vencord.dev/)
[![Status](https://img.shields.io/badge/Status-Working%20(2026)-75a00d?style=for-the-badge)](#)

> **"Get Good, Get GameSense."**  
> An authentic GameSense / Skeet aesthetic custom theme for Discord, rewritten and fully updated for modern Discord updates and the Desktop Visual Refresh.

---

## 📌 About This Project

This project is a modernized fix and continuation of the original [**Shaxzy/gamesense-discordtheme**](https://github.com/Shaxzy/gamesense-discordtheme/).

### Why the original stopped working
The original theme created by Shaxzy was built using hardcoded obfuscated CSS class hashes (like `.chat-3bRxxu`, `.appMount-3lHmkl`, `.inner-zqa7da`) from older Discord builds. As Discord pushed major client overhauls and migrated to the **Desktop Visual Refresh**, all of those class names were removed. Because the only rule not tied to an obsolete class was `* { font-family: ... }`, **only the font was working while all colors, borders, headers, and backgrounds remained default Discord**.

### What this fixed version brings
* **Native Discord Token Engine:** Maps the full GameSense color palette into modern Discord design tokens (`--bg-base-primary`, `--background-primary`, `--brand-500`, etc.), ensuring full coverage across all chat, sidebars, popouts, and settings.
* **Future-Proof Selectors:** Uses wildcard attribute selectors (`[class*="..."]`) instead of brittle hashes so future Discord client updates will not break the layout.
* **Modern Client Compatibility:** Fully updated metadata header (`/** @name ... */`) compatible with **BetterDiscord**, **Vencord**, **Vesktop**, and **Replugged**.
* **Preserved Authenticity:** Faithfully retains all the classic GameSense / Skeet details: the iconic rainbow gradient bar, the `game` + `sense` Raleway wordmark, double-inset input borders, sharp technical corners, and acid green accents.

---

## ✨ Features

- 🌈 **Signature Rainbow Top Bar:** The classic cyan $\rightarrow$ magenta $\rightarrow$ lime gradient line (`linear-gradient(to right, #37b1da, #c948cd, #cce335)`) running cleanly across the top edge.
- 🏷️ **GameSense Logo Wordmark:** Replaces the Discord logo with the iconic **game** (white) and **sense** (lime green) typography in Raleway.
- 🔲 **Skeet Menu Frame Outline:** Multi-layered dark charcoal frame (`box-shadow: 0 0 0 1px #3c3c3c, 0 0 0 4px #282828, 0 0 0 5px #3c3c3c, 0 0 0 6px #0a0a0a;`).
- 🟢 **Channel List & Active Highlight:** Selected channels illuminate with a `#191919` dark card and glowing `#9fca2b` green text and icons.
- 💬 **Custom Chat Input:** Double-inset technical border (`box-shadow: inset 0 0 0 1px #323232, inset 0 0 0 2px #101010;`).
- 📜 **Custom 6px Scrollbars:** Crisp, rectangular dark scrollbars (`#2d2d2d` track, `#414141` thumb).
- 🎚️ **Gamesense Sliders & Toggles:** Sliders and checked toggles feature the classic gradient fill (`linear-gradient(to bottom, #99c427, #699404)`).
- 💻 **Syntax & Code Blocks:** Terminal-style `#232323` dark container with monospace font and subtle borders.
- 📐 **Anti-Bubble Aesthetic:** Replaces modern Discord bubble roundedness with sharp, compact, technical edges (`border-radius: 0` to `4px`).

---

## 🚀 Installation Guide

### 1. BetterDiscord
1. Download [`gamesense.theme.css`](./gamesense.theme.css).
2. Open Discord and navigate to **User Settings** (⚙️) $\rightarrow$ **Themes** (under the **BetterDiscord** section).
3. Click the **Open Themes Folder** button at the top.
4. Drag and drop `gamesense.theme.css` into that folder.
5. In Discord, turn the toggle switch **ON** for **GameSense Discord Theme**.

---

### 2. Vencord / Vesktop

#### Method A: Themes Folder (Recommended)
1. Download [`gamesense.theme.css`](./gamesense.theme.css).
2. Open Discord and navigate to **User Settings** (⚙️) $\rightarrow$ **Themes** (under the **Vencord** section).
3. Click **Open Themes Folder** and place `gamesense.theme.css` inside.
4. Click **Load Missing Themes** and enable it.

#### Method B: Online Theme Link
1. Go to **User Settings** (⚙️) $\rightarrow$ **Vencord** $\rightarrow$ **Themes**.
2. Under **Online Themes**, paste the raw GitHub link:
   ```text
   https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/gamesense.theme.css
   ```
3. Press Enter to apply.

#### Method C: QuickCSS
1. Copy the entire contents of [`gamesense.theme.css`](./gamesense.theme.css).
2. Go to **User Settings** (⚙️) $\rightarrow$ **Vencord** $\rightarrow$ **Vencord** $\rightarrow$ **Edit QuickCSS**.
3. Paste the code into the editor and save.

---

### 3. Replugged
1. Clone or download `gamesense.theme.css` into your Replugged themes directory:
   - **Windows:** `%APPDATA%\replugged\themes`
   - **Linux:** `~/.config/replugged/themes`
   - **macOS:** `~/Library/Application Support/replugged/themes`
2. Enable the theme under **User Settings** $\rightarrow$ **Replugged** $\rightarrow$ **Themes**.

---

## 🎨 Customization

You can easily adjust colors, fonts, or window radii by changing the CSS variables near the top of `gamesense.theme.css`:

```css
:root {
    /* Accent colors */
    --primary-color: #75a00d;             /* Main GameSense green accent */
    --channels-text-selected: #9fca2b;    /* Active channel text color */
    --link-color: #96c83c;                /* Hyperlink color */

    /* Backgrounds */
    --app-color: #111111;                 /* Base app background */
    --channels-color: #111111;            /* Channel list background */
    --channels-darker: #0c0c0c;           /* Server list & header background */
    --chat-color: #1a1a1a;                /* Chat message area background */
    --text-input: #191919;                /* Textarea input background */

    /* Typography & Corners */
    --font: 'Verdana', 'Tahoma', Helvetica, Arial, sans-serif;
    --channel-radius: 4px;                /* Corner radius for icons and pills */
}
```

---

## 📸 Preview

![GameSense Discord Theme Preview](https://i.gyazo.com/b1957bbcc8c7dd84c8b72bc038abd7f3.png)

---

## 📄 License

This theme is provided free of charge for the community. Distributed under the [MIT License](LICENSE).
