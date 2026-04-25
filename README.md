# ResumeIQ — AI Resume Compatibility Analyzer

> **A single-file, browser-based AI tool that scores and ranks resumes against a job description — instantly, privately, and for free.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Netlify-black?style=flat-square&logo=netlify)](https://resumeiq-compare-jd.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](./LICENSE)
[![No Install](https://img.shields.io/badge/No%20Install-Open%20in%20Browser-blue?style=flat-square)]()
[![Built-in OCR](https://img.shields.io/badge/OCR-Tesseract.js-orange?style=flat-square)]()

---

**ResumeIQ** is a modern, AI-powered recruitment tool designed to streamline the candidate screening process. By leveraging advanced Large Language Models (LLMs) and a specialized local parsing engine, it provides recruiters with deep insights into candidate suitability—all within a secure, browser-native environment.

---

## 🌐 Live Demo

👉 **[resumeiq-compare-jd.netlify.app](https://resumeiq-compare-jd.netlify.app/)** — Open, paste, analyze. No signup, no install.

---

## 🚀 Key Features

### 🧠 Layout-Aware Parsing Engine
ResumeIQ uses a specialized local engine to handle complex resume formats:
- **Spatial Reconstruction**: Preserves columns, sidebars, and complex layouts in PDFs for more accurate AI analysis.
- **Built-in OCR**: Automatically detects scanned PDFs and images (PNG, JPG), using Tesseract.js to extract text locally.
- **Universal Word Support**: Native `.docx` and `.doc` parsing via Mammoth.js for clean text extraction.

### 📊 Hybrid Scoring & ATS Analysis
Inspired by industry leaders like *Resume-Matcher* and *RAG-Anything*:
- **Markdown-Hierarchical Prompting**: Uses structured document segmentation to ensure AI never "drops" data during extraction.
- **ATS Buzzword Detection**: Automatically flags generic jargon (e.g., *synergy*, *rockstar*) and provides an **ATS Readability Score**.

### 🧠 Multi-Provider AI Engine
Connect to the world's most powerful AI models with ease:
- **7+ AI Provider Support**: Use your own API key for Google Gemini, Groq, NVIDIA NIM, OpenRouter, and more.
- **Default Public API**: Works out of the box with Pollinations AI.

### 💬 Intelligent AI Assistant
- **Candidate Comparison**: Ask "Why is Candidate A a better fit than Candidate B?" for instant comparisons.
- **Interview Prep**: Generate targeted interview questions based on candidate gaps.

## 🤖 Supported AI Providers

| Provider | Key Required | Model Used | Notes |
|---|---|---|---|
| **Pollinations AI** | ❌ None | `openai` (public) | **Default** — May be slow |
| **Google Gemini** | ✅ Free | `gemini-3.1-flash-lite` | [Get key](https://aistudio.google.com) — **Recommended** |
| **Groq** | ✅ Free | `llama-3.3-70b-versatile` | [Get key](https://console.groq.com) |
| **OpenRouter** | ✅ Free | `llama-3.3-70b-instruct:free` | [Get key](https://openrouter.ai) |

---

## 📄 How It Works

```
Upload Resumes (PDF/Word/Images/Text)
        ↓
Local Parsing Engine (Browser-side)
        ↓
Analysis Engine (Hybrid AI + Heuristic)
        ↓
Render Carousel & Table Results
        ↓
Export PDF Report (optional)
```

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Structure** | HTML5 Semantic Markup |
| **Logic** | Vanilla JavaScript (ES6+) |
| **PDF Engine** | [PDF.js](https://mozilla.github.io/pdf.js/) |
| **OCR Engine** | [Tesseract.js](https://tesseract.projectnaptha.com/) |
| **Word Engine** | [Mammoth.js](https://github.com/mwilliamson/js-mammoth) |

---

**Built with precision by [opsengine-sys](https://github.com/opsengine-sys)**. *All rights reserved.*
