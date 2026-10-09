# 🏥 MedGemma 27B-IT Diagnostic Hub

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Modal](https://img.shields.io/badge/Deployed_on-Modal.com-black?logo=modal)
![GPU](https://img.shields.io/badge/Compute-NVIDIA_H100_/_A100-76B900?logo=nvidia)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![PWA](https://img.shields.io/badge/PWA-Supported-purple.svg)

An enterprise-grade, decoupled AI diagnostic application leveraging Google's **MedGemma 27B** vision-language model. This platform bridges serverless GPU cloud infrastructure with a progressive web and desktop interface designed for rapid, multimodal biomedical analysis and clinical reporting.

Developed as an academic research project in Biomedical Engineering Technology, this platform aims to democratize open-weights medical AI for clinical and research environments.

---

## ✨ Features & Architecture

* **Multimodal Clinical Inference:** Real-time evaluation combining medical imaging (X-rays, CT scans, MRIs) with detailed textual queries using `google/medgemma-27b-it`.
* **Serverless H100/A100 GPU Backend:** Hosted on Modal.com with Scaled Dot Product Attention (SDPA) and dynamic image resolution scaling to optimize token encoding.
* **Smart Compute Efficiency:** Features client-driven session management and idle container timeouts on Modal to ensure compute credits are strictly used during active inference.
* **Web & PWA Client:** Progressive Web App interface featuring service worker support (`sw.js`), custom assets, and responsive UI components.

---

## 🏗️ System Overview
