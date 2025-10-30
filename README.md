# 🕵️‍♂️ Rahasya — DWT-DCT Image Steganography (Frontend)

> “Where Every Pixel Speaks in Silence”  
> **Author:** Aryan Patel  
> **Year:** 2025  
> **Domains:** Digital Image Processing (DIP) + Cloud Computing  
> **Frontend (Live):** [https://rahasya.netlify.app](https://rahasya.netlify.app)  
> **Backend API:** [https://stego-backend-l72r.onrender.com](https://stego-backend-l72r.onrender.com)

---

## 📘 Project Overview
**Rahasya** is a cloud-based image steganography system that securely hides a **secret image inside a cover image** using a **hybrid DWT-DCT (Discrete Wavelet Transform + Discrete Cosine Transform)** technique.  
This repository contains the **frontend** — a web-based interface built using HTML, CSS, and JavaScript.  

The project demonstrates a practical fusion of **Digital Image Processing** and **Cloud Computing**, where:
- Image processing runs on a cloud-hosted Flask API (Render).  
- The user interface runs on a globally available static site (Netlify).  

---

## 🎯 Objectives
- Implement image steganography using the **DWT-DCT hybrid model**.  
- Build a user-friendly browser-based interface for encoding and decoding images.  
- Deploy both frontend and backend entirely on **cloud platforms** (Netlify + Render).  
- Demonstrate global accessibility — accessible “anytime, anywhere”.

---

## 🧠 Core Concepts

### 🧩 Digital Image Processing (DWT + DCT)
- **DWT (Discrete Wavelet Transform):** Decomposes the image into frequency subbands (LL, LH, HL, HH).
- **DCT (Discrete Cosine Transform):** Embeds data in mid-frequency coefficients for better robustness.
- The **secret image** is embedded in the **cover image’s DWT-DCT domain**, producing a visually identical **stego image**.
- The inverse DWT and DCT reconstruct the image to retrieve the hidden secret.

### ☁️ Cloud Computing
- **Frontend:** Deployed on **Netlify Cloud** for global static hosting.  
- **Backend:** Flask API hosted on **Render Cloud** for processing requests.  
- Together, they form a **two-tier cloud system** demonstrating distributed cloud integration.

---

## ⚙️ Technologies Used
| Category | Tools / Tech |
|-----------|--------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend API | Flask, NumPy, Pillow, PyWavelets |
| Cloud Hosting | Netlify (Frontend), Render (Backend) |
| Communication | Fetch API (REST calls) |
| Design | CSS gradients, responsive layout |
| Fonts | Inter (Google Fonts) |

---

## 🚀 How It Works (User Steps)
1. **Open:** [https://rahasya.netlify.app](https://rahasya.netlify.app)
2. **Upload Cover Image:** Base image in which data will be hidden.
3. **Upload Secret Image:** The image to embed.
4. Click **Encode** → The app sends both images to the backend API.  
   → Backend applies DWT-DCT embedding → Returns the **stego image**.
5. Download the stego image (`stego.png`).
6. To **decode**, upload the stego image and click **Decode** → Extracted secret image is shown and downloadable.

---

## 🧩 System Architecture
```mermaid
flowchart TD
    User[Web Browser<br>(Frontend)] -->|Uploads images| FE[Netlify Frontend]
    FE -->|POST /encode, /decode| BE[Flask API<br>(Render Cloud)]
    BE -->|DWT + DCT Processing| IMG[Image Processing Engine]
    IMG -->|Stego/Secret PNG| FE

---

## ☁️ Cloud Workflow

| Layer | Platform | Description |
|--------|-----------|-------------|
| **Frontend** | Netlify | Hosts the static web interface (HTML, JS, CSS) |
| **Backend** | Render Cloud | Flask API processes steganography encode/decode requests |
| **Transport Layer** | HTTPS | Secure REST API calls between Netlify and Render |
| **User Access** | Global | Anyone can access from any device, anywhere |

The project architecture demonstrates **distributed cloud integration**, where each layer (frontend and backend) runs on separate cloud platforms that communicate securely via HTTPS.

---

## 💻 Local Testing (Optional)

You can also run the project locally before deploying:

1. Clone this repository:
   ```bash
   git clone https://github.com/wolfking05/stego-frontend.git
   cd stego-frontend

2. Open the file **index.html** directly in your web browser.  
   - You can simply double-click it, or  
   - Run a local server using Python:
     ```bash
     python -m http.server 8000
     ```
     Then open: [http://localhost:8000](http://localhost:8000)

3. Make sure your backend API link inside `index.html` points to your Render deployment:

   ```html
   <span id="backendUrl">https://stego-backend-l72r.onrender.com</span>

If successful, both commands return a valid .png file without any errors.

---

✅ **Then continue immediately with the next section:**

---

```md
---

## 🧾 Cloud Concepts Demonstrated

- **Platform as a Service (PaaS):** Render hosts the Flask-based backend API.  
- **Software as a Service (SaaS):** Netlify delivers the frontend globally.  
- **Distributed Cloud Integration:** Frontend and backend communicate over HTTPS between two different cloud providers.  
- **Scalability:** Each component can scale independently on demand.  
- **Serverless Frontend:** The web UI runs directly from the CDN — no dedicated server required.  
- **Global Accessibility:** Application can be accessed from any device, anywhere, with an internet connection.

---

## 🧩 Repository Structure

stego-frontend/
├── index.html # Main single-page web application
├── assets/ # (Optional) static icons, images
└── README.md # Documentation file


---

## 📊 Performance Metrics

| Metric | Description |
|---------|--------------|
| **PSNR (Peak Signal-to-Noise Ratio)** | > 40 dB — Excellent imperceptibility |
| **MSE (Mean Squared Error)** | Very low — minimal distortion between cover and stego images |
| **Embedding Capacity** | Supports full-color (RGB) images |
| **Execution Time** | Typically < 1 second for 512×512 images |
| **Cloud Response Time** | ~300–800 ms (via Render Flask API) |

---

## 🧑‍🏫 Academic Relevance

This project bridges **Digital Image Processing** and **Cloud Computing**, making it ideal for academic demonstration.

### Digital Image Processing (DIP)
- Implements **hybrid DWT-DCT** frequency-domain embedding.  
- Preserves image quality while embedding secret data.  
- Demonstrates transform-domain steganography techniques.

### Cloud Computing
- **Frontend (SaaS):** Delivered as a globally accessible service using Netlify.  
- **Backend (PaaS):** Flask REST API deployed on Render Cloud.  
- Demonstrates **inter-cloud communication** and **scalable architecture**.  
- Enables **on-demand, location-independent** access to image processing services.

---

## 🧩 Results

- Secret images embedded and extracted with **zero visible distortion**.  
- Achieved **PSNR > 40 dB** and low MSE values, ensuring quality retention.  
- Fully functional **cloud-deployed** application accessible worldwide.  
- Demonstrated hybrid DWT-DCT steganography and cloud integration effectively.

---

## 🧠 Future Enhancements

- Extend DWT-DCT to support **video steganography**.  
- Integrate **encryption (AES)** for enhanced data security.  
- Use **cloud object storage (AWS S3 / Google Cloud Storage)** for persistent image handling.  
- Add **user authentication** for privacy and usage tracking.

---

## 🧑‍💻 Contributors

| Name | Role | Domain |
|------|------|--------|
| **Aryan Patel** | Developer | Digital Image Processing + Cloud Computing |

---

## 📜 License

© 2025 **Aryan Patel** — All Rights Reserved.  
For educational and demonstrative use only.

---

