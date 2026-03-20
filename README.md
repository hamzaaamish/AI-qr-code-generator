# QR·AI — Intelligent QR Code Generator

> *Turn any idea into a scannable QR code — powered by Claude AI*

---

## About the Project

**QR·AI** is a browser-based, AI-powered QR code generator that goes beyond simple text encoding. Instead of just converting raw text into a QR code, it uses **Claude (Anthropic's AI)** to understand your intent, enhance your input, and generate the most appropriate scannable content automatically.

Whether you type *"my portfolio website"*, *"WiFi for my coffee shop"*, or *"contact card for Hamza, developer"* — QR·AI figures out exactly what to encode, formats it correctly, and produces a styled QR code that links to a beautiful hosted display page.

No backend. No database. No installation. Just two HTML files.

---

## Features

- **AI-Powered Processing** — Claude AI understands natural language and converts it into proper QR-encodable formats (URLs, WiFi configs, vCards, plain messages)
- **3 Smart Modes** — Smart Auto-detect, Enhance existing input, or Generate from a vague idea
- **Hosted Display Page** — QR codes don't just encode raw text; they link to a real webpage (`display.html`) that renders the content beautifully when scanned
- **Content-Aware Display** — The display page automatically detects whether the content is a URL, WiFi network, contact card, or message — and shows the right UI for each
- **6 QR Color Themes** — Charcoal, Forest, Walnut, Slate Blue, Mauve, Umber
- **Download & Copy** — Export the QR as PNG or copy the encoded content
- **Recent History** — Last 6 generated QR codes stored in-session for quick access
- **Zero Backend** — Everything runs in the browser; content is passed via URL parameters

---

## How It Works

```
You type: "WiFi for my cafe, network BrewCo, password latte123"
         ↓
  Claude AI processes it
         ↓
  Generates: WIFI:T:WPA;S:BrewCo;P:latte123;;
         ↓
  QR encodes: https://yoursite.github.io/qr-ai/display.html?msg=WIFI:...
         ↓
  Someone scans the QR code
         ↓
  display.html opens → shows WiFi name + password in a clean card UI
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| AI / Language Model | Claude (claude-sonnet-4) via Anthropic API |
| QR Generation | qrcode.js (browser-side) |
| Frontend | Vanilla HTML, CSS, JavaScript |
| Fonts | Instrument Serif + DM Mono (Google Fonts) |
| Hosting | GitHub Pages (free static hosting) |
| Backend | None — fully client-side |

---

## Project Structure

```
qr-ai/
├── index.html      ← QR Generator UI (AI input + QR output)
├── display.html    ← Hosted display page (shown when QR is scanned)
└── SETUP.md        ← GitHub Pages hosting guide
```

---

## Getting Started

### Prerequisites
- An [Anthropic API key](https://console.anthropic.com) (free tier available)
- A GitHub account (for hosting)

### Run Locally
Just open `index.html` in any modern browser. No server needed.

### Host on GitHub Pages
See [`SETUP.md`](./SETUP.md) for the full 5-minute hosting guide.

---

## Use Cases

- **Personal portfolio** — Encode your portfolio link into a printable QR for resumes or business cards
- **Event networking** — Share your contact card via QR at meetups or hackathons
- **Cafe / office WiFi** — Print a QR code that shows your WiFi name and password when scanned
- **Product packaging** — Encode a product message or landing page link
- **Creative messaging** — Share a handwritten-style message through a QR scan

---

## Limitations

- Content is passed via URL parameters — very long text (1000+ chars) may not encode reliably in QR
- Requires an Anthropic API key; API calls are made directly from the browser
- No persistent storage — history resets on page refresh

---

## Made with

- [Claude AI](https://anthropic.com) by Anthropic
- [qrcode.js](https://github.com/davidshimjs/qrcodejs)
- [Google Fonts](https://fonts.google.com) — Instrument Serif & DM Mono

---

*Built as a real-time AI + QR project — no frameworks, no servers, just ideas turned into code.*
