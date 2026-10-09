# 🏥 MedGemma-27B-IT Diagnostic Hub

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Modal](https://img.shields.io/badge/Deployed_on-Modal.com-black?logo=modal)
![GPU](https://img.shields.io/badge/Compute-NVIDIA_H100-76B900?logo=nvidia)
![License](https://img.shields.io/badge/License-MIT-green.svg)

An AI-driven biomedical diagnostic hub leveraging Google's **MedGemma 27B** vision-language model. This project provides a robust, universal Windows desktop client connected to a serverless H100 GPU backend, designed for rapid, multimodal clinical data analysis.

Developed as a Final Year Project in Biomedical Engineering Technology, this system bridges the gap between massive open-weights medical AI and accessible clinical hardware.

---

## ✨ Key Features

*   **Multimodal Inference:** Process complex clinical queries alongside high-resolution medical imaging (X-rays, MRIs, CT scans) using `google/medgemma-27b-it`.
*   **Serverless H100 Acceleration:** Backend deployed on Modal.com utilizing an NVIDIA H100 GPU. Integrated with Scaled Dot Product Attention (SDPA) for lightning-fast token generation and image processing.
*   **Cost-Optimized Architecture:** Features a manual "Wake GPU" mechanism via the desktop client to prevent cloud credit drain, maintaining a strict 20-minute idle timeout.
*   **Universal Desktop Client:** A compiled, self-signed 32-bit/64-bit universal Windows `.exe` built with CustomTkinter, designed to run securely on restricted hospital PCs bypassing SmartScreen warnings.
*   **Smart Document Parsing:** Automatic text extraction from clinical PDF reports utilizing `PyMuPDF`.
*   **Automated Clinical Reporting:** Instantly export AI diagnostic insights and conversation history into professionally formatted PDF reports via `fpdf`.

## 🏗️ System Architecture

The hub operates on a decoupled client-server architecture:

```mermaid
graph LR
    A[Desktop Client <br> CustomTkinter] -->|Base64 Images + Text | B(Modal.com <br> Serverless Endpoint);
    B -->|SDPA Optimized Inference| C{NVIDIA H100 <br> 80GB VRAM};
    C -->|MedGemma 27B| B;
    B -->|JSON Response| A;
