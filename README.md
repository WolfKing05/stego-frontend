# 🕵️‍♂️ Rahasya — Where Every Pixel Speaks in Silence

Rahasya is a modern web-based **image steganography tool** that allows users to hide and reveal secret images within other images using intelligent pixel-level encoding — right from the browser.

It blends **visual elegance**, **cloud integration**, and **privacy-centric design** in a single, minimal interface.

---

## 🌐 Live Deployment

🔗 **Frontend (GitHub Pages):** [https://wolfking05.github.io/stego-frontend/](https://wolfking05.github.io/stego-frontend/)  
⚙️ **Backend (Render):** [https://stego-backend-l72r.onrender.com](https://stego-backend-l72r.onrender.com)

---

## ✨ Features

- 🔐 **Encode Mode:** Hide a secret image inside a cover image.
- 🧩 **Decode Mode:** Reveal the hidden image from the stego image.
- 🌙 **Light & Dark Themes:** Seamless toggle with blue neon accents.
- 💎 **Right+Bottom Neon Glow:** Dynamic depth effect on hover.
- 🕓 **Encode/Decode History:** Persistent local storage of results.
- ⚡ **Responsive, Lightweight & Fast:** Works on any browser.
- 🔔 **Toast Notifications:** Real-time user feedback.

---

## 🧠 Tech Stack

| Layer | Technology |
|--------|-------------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Design** | Pastel light blue & neon dark blue theme |
| **Hosting** | GitHub Pages |
| **API** | Flask backend (Render) via Fetch API |

---

## 🗂️ Project Structure
stego-frontend/
│
└── index.html # Main frontend

---

## 🔗 Backend Integration

Backend API endpoints (Flask):

| Endpoint | Method | Description |
|-----------|---------|-------------|
| `/encode` | POST | Accepts `cover` + `secret` → Returns `stego.png` |
| `/decode` | POST | Accepts `stego` → Returns `extracted.png` |

Configured inside `index.html`:
```js
const BACKEND = "https://stego-backend-l72r.onrender.com";


