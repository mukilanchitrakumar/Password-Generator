<div align="center">

# 🔐 VAULTKEY

### A Modern, Feature-Rich Password Generator

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-00e5ff?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**100% client-side · Zero dependencies · Zero data collection**

[Live Demo](https://mukilanchitrakumar.github.io/Password-Generator/) · [Report Bug](../../issues) · [Request Feature](../../issues)

</div>

---

## ✨ Overview

VAULTKEY is a fully-featured, single-file password generator built with pure HTML, CSS, and JavaScript. It runs entirely in your browser — no server, no tracking, no data ever leaves your device.

Designed with a dark cyber aesthetic and packed with security tooling, it gives you full control over how your passwords are generated and helps you understand exactly how strong they are.

---

## 🚀 Features

### 4 Generation Modes

| Mode | Description | Example |
|------|-------------|---------|
| **Random** | Fully customizable character-based password | `xK#9mQp!rL2vN$4w` |
| **Passphrase** | Word-based, easy to remember | `apple-river-storm-bold` |
| **PIN** | Numeric codes, configurable length | `847291` |
| **Memorable** | Pronounceable syllable patterns | `Tifonu82` |

### Character Set Controls (Random Mode)
- Toggle **Uppercase**, **Lowercase**, **Numbers**, **Symbols** independently
- Exclude **similar-looking characters** (`0`, `O`, `o`, `l`, `1`, `I`)
- Exclude **ambiguous characters** (`{`, `}`, `[`, `]`, `(`, `)`)
- Add a **custom character pool** (e.g. `€ £ ¥ →`)
- **Exclude specific characters** you want to avoid
- Options: **Begin with a letter**, **No repeating characters**

### Passphrase Controls
- Adjustable word count (2–10 words)
- Separator options: dash `-`, dot `.`, underscore `_`, or none
- Optional capitalization and appended random numbers

### Security Analytics
- **Real-time strength meter** with label (Very Weak → Exceptional)
- **Entropy score** in bits with visual segment display
- **Time to crack** estimates at 4 realistic attack speeds:
  - Online attack (1,000/s)
  - Offline hash attack (1 Billion/s)
  - GPU cluster (1 Trillion/s)
  - Nation-state (1 Quadrillion/s)
- **Character breakdown chart** showing composition at a glance

### Productivity Features
- **Click-to-copy** on the password display
- **Bulk generate** up to 50 passwords at once with copy-all
- **Password history** — save, copy, and delete individually (persisted via `localStorage`)
- **Keyboard shortcuts**: `Ctrl+Enter` to generate, `Ctrl+C` to copy

---

## 📸 Preview

> *Dark cyber aesthetic with animated grid background, glowing accents, and smooth micro-interactions.*

```
┌─────────────────────────────────────────────┐
│  🔐 VAULTKEY                  v2.0 CLIENT-SIDE │
├─────────────────────────────────────────────┤
│  [ Random ] [ Passphrase ] [ PIN ] [Memorable]│
│                                             │
│  Strength ████████████░░░░  Very Strong     │
│  ┌─────────────────────────────────────┐   │
│  │  xK#9mQp!rL2vN$4w                  │   │
│  └─────────────────────────────────────┘   │
│  [ ⚡ Generate ]  [ 📋 Copy ]  [ 💾 Save ]  │
│                                             │
│  Entropy: 104 bits   Crack: ∞ centuries     │
└─────────────────────────────────────────────┘
```

---

## 🛠️ Getting Started

### Option 1 — Just open it
Download `password-generator.html` and open it in any modern browser. That's it.

```bash
git clone https://github.com/yourusername/vaultkey.git
cd vaultkey
open password-generator.html   # macOS
# or double-click the file on Windows/Linux
```

### Option 2 — Serve locally
```bash
# Python
python -m http.server 8080

# Node.js
npx serve .
```

Then visit `http://localhost:8080/password-generator.html`

---

## 🔒 Privacy & Security

- **100% client-side** — all generation happens in your browser using the Web Crypto API (`crypto.getRandomValues`)
- **No network requests** — the page makes zero external calls after loading fonts from Google Fonts
- **No analytics, no telemetry, no ads**
- **No data ever leaves your device** — passwords are never transmitted anywhere
- History is stored only in your own browser's `localStorage` and can be cleared at any time

> **Note:** For maximum privacy, you can download the font files locally and remove the Google Fonts `<link>` tag from the HTML.

---

## 🏗️ Tech Stack

- **Pure HTML5 / CSS3 / Vanilla JavaScript** — zero frameworks, zero build tools
- **Web Crypto API** — cryptographically secure random number generation
- **CSS Custom Properties** — for the full theming system
- **CSS Animations** — grid background, orb effects, glitch reveal, micro-interactions
- **localStorage** — for persisting password history client-side
- **Google Fonts** — Syne (display) + JetBrains Mono (monospace)

---

## 📁 Project Structure

```
vaultkey/
└── password-generator.html    # The entire app — self-contained single file
```

---

## 🎨 Design

VAULTKEY uses a **dark cyber aesthetic** with:
- Deep navy/dark blue background with animated CSS grid
- Floating radial blur orbs for depth
- `#00e5ff` cyan as the primary accent with green (`#00ffb3`) and red (`#ff4d6d`) for status
- **Syne** for headings — geometric, modern, bold
- **JetBrains Mono** for passwords and data — technical, clear, readable
- Character-by-character password reveal animation on generation
- Smooth strength bar and entropy segment transitions

---

## 🧮 How Entropy is Calculated

```
Entropy (bits) = log₂(pool_size ^ password_length)
```

Where `pool_size` is the number of unique characters available based on your selected options. A higher entropy means exponentially more combinations an attacker must try.

| Entropy | Strength |
|---------|----------|
| < 40 bits | Very Weak |
| 40–60 bits | Weak / Fair |
| 60–80 bits | Good |
| 80–100 bits | Very Strong |
| 100+ bits | Exceptional |

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Generate new password |
| `Ctrl + C` | Copy current password (when not in input) |
| Click password | Copy to clipboard |

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">

Made with 🔐 and pure JavaScript · No frameworks harmed in the making of this tool

</div>
