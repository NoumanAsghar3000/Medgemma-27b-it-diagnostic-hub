# 🏥 MedGemma 27B-IT Diagnostic Hub

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Modal](https://img.shields.io/badge/Deployed_on-Modal.com-black?logo=modal)
![GPU](https://img.shields.io/badge/Compute-NVIDIA_H100_/_A100-76B900?logo=nvidia)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Build](https://img.shields.io/badge/Architecture-Universal_x86%2Fx64-orange)

An enterprise-grade, decoupled AI diagnostic application leveraging Google's **MedGemma 27B** vision-language model. This system bridges high-performance serverless GPU cloud infrastructure with an optimized desktop client designed for rapid, multimodal biomedical analysis and clinical reporting.

Developed as an academic research project in Biomedical Engineering Technology, this platform aims to democratize advanced open-weights medical AI for clinical environments.

---

## ✨ System Features

* **Multimodal Vision-Language Inference:** Real-time clinical evaluation combining high-resolution medical imaging (X-rays, CT scans, MRIs) with descriptive medical prompts using `google/medgemma-27b-it`.
* **High-Performance Serverless Backend:** Hosted on Modal.com with Scaled Dot Product Attention (SDPA) and dynamic 1024x1024 image resolution optimization, minimizing inference latency to seconds.
* **Smart Credit Preservation:** Features a client-side manual "Wake GPU" mechanism paired with a 20-minute backend idle container timeout to eliminate unnecessary compute consumption.
* **Universal Desktop Client:** Standardized Windows GUI built with `CustomTkinter`, compiled into a single executable and digitally signed via X.509 code signing with Sectigo timestamping to bypass SmartScreen restrictions.
* **Clinical Data Integration:** Native PDF parsing using `PyMuPDF` and automated PDF diagnostic export generation powered by `fpdf`.

---

## 🏗️ Technical Architecture
