# ♻️ PlasticDetect AI

[![Live Demo](https://img.shields.io/badge/Live_Demo-GitHub_Pages-2ea44f?style=for-the-badge&logo=github)](https://omukinkar18-hub.github.io/plasticdetect-ai/)
[![TensorFlow.js](https://img.shields.io/badge/TensorFlow.js-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/js)
[![Teachable Machine](https://img.shields.io/badge/Google_Teachable_Machine-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://teachablemachine.withgoogle.com/)
[![PWA](https://img.shields.io/badge/PWA-Ready-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)](https://web.dev/progressive-web-apps/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> 🚀 **Live Web App:** [https://omukinkar18-hub.github.io/plasticdetect-ai/](https://omukinkar18-hub.github.io/plasticdetect-ai/)

An intelligent, privacy-first **Progressive Web Application (PWA)** that detects and classifies plastic waste categories in real-time directly on your mobile device using **TensorFlow.js** and **MobileNetV2**.

---

## 🌟 Key Features

- 🔒 **100% On-Device & Privacy-Preserving:** AI inference runs entirely client-side in the browser via TensorFlow.js — no images or camera feeds are ever sent to an external server.
- 🏷️ **9 Plastic Resin Classifications:** Identifies PET, HDPE, PVC, LDPE, PP, PS, PLA, ABS, and PC with real-time confidence scores.
- 📱 **Mobile-First Progressive Web App (PWA):** Installable on Android & iOS home screens with full offline support enabled by service worker caching.
- ♻️ **Recycling & Disposal Guide:** Provides recycling recommendations, resin codes, and decomposition insights for detected plastic types.
- 🌓 **Modern UI:** Responsive design with smooth animations, dark/light theme switching, and live camera / photo upload support.
- 🛡️ **Heuristic Fallback:** Intelligent fallback mechanism ensuring graceful degradation if WebGL or model initialization fails.

---

## 🧠 AI Pipeline & Dataset Curation

1. **Dataset Collection:** 
   - Manually curated and labeled image datasets gathered across real-world plastic items, resin codes, packaging materials, and varying lighting conditions.
2. **Model Training:**
   - Trained via **Google Teachable Machine** using transfer learning on a **MobileNetV2** deep convolutional neural network backbone.
3. **Model Export & Optimization:**
   - Converted into TensorFlow.js graph model format (`model.json` + binary weights) for fast, hardware-accelerated WebGL inference in mobile browsers.

---

## 🏗️ Architecture & Tech Stack

```
plasticdetect-ai/
├── index.html            # Main UI & responsive interface
├── manifest.json         # PWA configuration & app metadata
├── service-worker.js     # Offline caching for assets & model weights
├── css/
│   └── styles.css        # Responsive styling & theme variables
├── js/
│   ├── app.js            # UI controller, camera streams & event handling
│   ├── classifier.js     # TensorFlow.js model loader & inference engine
│   ├── data.js           # Plastic resin knowledge base & disposal guide
│   └── model/            # Trained TF.js model files & class mappings
│       ├── model.json
│       ├── weights.bin
│       └── class_map.json
└── icons/                # PWA app icons
```

| Component | Technology |
|---|---|
| **Frontend** | Vanilla JavaScript (ES6+), HTML5, CSS3 |
| **Machine Learning** | TensorFlow.js, MobileNetV2, Google Teachable Machine |
| **Offline & Storage** | Service Workers, Cache API, Web Manifest |
| **Acceleration** | WebGL / GPU-accelerated browser execution |

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/omukinkar18-hub/plasticdetect-ai.git
cd plasticdetect-ai
```

### 2. Run locally
Start any local HTTP server:

```bash
# Using Python
python3 -m http.server 8000

# Or using Node.js / npx
npx serve .
```

Open `http://localhost:8000` in your browser.

> [!NOTE]
> Accessing the camera requires a secure context (`localhost` or `HTTPS`). For testing on mobile devices, deploy via GitHub Pages or an HTTPS-enabled host.

---

## 🤝 Contributing

Contributions, feedback, and dataset expansions are welcome! Feel free to open an issue or submit a pull request.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
