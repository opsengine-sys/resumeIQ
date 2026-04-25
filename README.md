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

### 🧠 Multi-Provider AI Engine
Connect to the world's most powerful AI models with ease:
- **7+ AI Provider Support**: Use your own API key for Google Gemini, Groq, NVIDIA NIM, OpenRouter, and more.
- **Smart Fallback**: Automatically cycles through free models (via OpenRouter) if one is overloaded.
- **Custom Endpoints**: Fully compatible with any OpenAI-standard API (Ollama, LM Studio).

### 💬 Intelligent AI Assistant
Go beyond simple scoring. Our built-in chat assistant allows you to interact with your data:
- **Candidate Comparison**: Ask "Why is Candidate A a better fit than Candidate B?" for instant, tabulated comparisons.
- **Interview Prep**: Generate targeted interview questions based on a candidate's specific gaps or strengths.
- **Deep Dives**: Query specific details about experience or educational background.

### 📊 Professional Analytics & Reporting
- **Multi-Resume Analysis**: Upload up to 10 resumes (PDF, Word, Images, TXT, RTF, MD) and rank them all at once.
- **Automated Ranking**: Instantly sort candidates based on a weighted compatibility score.
- **Premium PDF Export**: Generate boardroom-ready hiring reports with consistent branding and recruiter insights.
- **Carousel + Table Views**: Visualize results side-by-side or in a sortable table.

---

## 🤖 Supported AI Providers

| Provider | Key Required | Model Used | Notes |
|---|---|---|---|
| **Pollinations AI** | ❌ None | `openai` (public) | Default — works instantly |
| **Google Gemini** | ✅ Free | `gemini-3.1-flash-lite` | [Get key](https://aistudio.google.com) |
| **Groq** | ✅ Free | `llama-3.3-70b-versatile` | [Get key](https://console.groq.com) |
| **NVIDIA NIM** | ✅ Free credits | `llama-3.3-70b-instruct` | [Get key](https://build.nvidia.com) |
| **OpenRouter** | ✅ Free | `llama-3.3-70b-instruct:free` | [Get key](https://openrouter.ai) — auto-fallback |
| **OpenAI** | 💳 Paid | `gpt-4o-mini` | New accounts get $5 credit |
| **Anthropic Claude** | 💳 Paid | `claude-sonnet-3.5` | Industry-leading quality |

---

## 📄 How It Works

```
Upload Resumes (PDF/Word/Images/Text)
        ↓
Local Parsing Engine (Browser-side)
├─ Layout-Aware PDF extraction
├─ Mammoth.js for Word Documents
└─ Tesseract.js OCR (for scanned docs)
        ↓
Build Analysis Prompt (Resume + Job Description)
        ↓
Send to AI Provider (your chosen API)
        ↓
Parse JSON Response → Score + Rank
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
| **Styling** | Vanilla CSS3 (Glassmorphism, Dynamic Transitions) |
| **Logic** | Vanilla JavaScript (ES6+) |
| **PDF Engine** | [PDF.js](https://mozilla.github.io/pdf.js/) (Layout-Aware Mode) |
| **OCR Engine** | [Tesseract.js](https://tesseract.projectnaptha.com/) |
| **Word Engine** | [Mammoth.js](https://github.com/mwilliamson/js-mammoth) |
| **Typography** | Playfair Display & Outfit |

---

## 📁 Repository Structure

```
resumeIQ/
├── index.html   # The entire application (single file)
├── README.md
└── LICENSE
```

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

**Built with precision by [opsengine-sys](https://github.com/opsengine-sys)**. *All rights reserved.*
