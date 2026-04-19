# ResumeIQ — AI Resume Compatibility Analyzer

> **A single-file, browser-based AI tool that scores and ranks resumes against a job description — instantly, privately, and for free.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Netlify-black?style=flat-square&logo=netlify)](https://resumeiq-compare-jd.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](./LICENSE)
[![No Install](https://img.shields.io/badge/No%20Install-Open%20in%20Browser-blue?style=flat-square)]()
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-green?style=flat-square)]()

---

**ResumeIQ** is a modern, AI-powered recruitment tool designed to streamline the candidate screening process. By leveraging advanced Large Language Models (LLMs), it provides recruiters and hiring managers with deep insights into candidate suitability, technical skill alignment, and experience depth—all within a secure, browser-native environment.

---

## 🌐 Live Demo

👉 **[resumeiq-compare-jd.netlify.app](https://resumeiq-compare-jd.netlify.app/)** — Open, paste, analyze. No signup, no install.

---

## 🚀 Key Features

### 🧠 Multi-Provider AI Engine
Connect to the world's most powerful AI models with ease. ResumeIQ supports a wide range of providers:
- **7+ AI Provider Support**: Use your own API key for Google Gemini, Groq, NVIDIA NIM, OpenRouter, and more.
- **Smart Fallback**: Automatically cycles through free models (via OpenRouter) if one is overloaded.
- **Custom Endpoints**: Fully compatible with any OpenAI-standard API (Ollama, LM Studio).

### 💬 Intelligent AI Assistant
Go beyond simple scoring. Our built-in chat assistant allows you to interact with your data:
- **Candidate Comparison**: Ask "Why is Candidate A a better fit than Candidate B?" for instant, tabulated comparisons.
- **Interview Prep**: Generate targeted interview questions based on a candidate's specific gaps or strengths.
- **Deep Dives**: Query specific details about experience or educational background.

### 📊 Professional Analytics & Reporting
- **Multi-Resume Analysis**: Upload up to 10 resumes (PDF, DOCX, TXT, RTF, MD) and rank them all at once.
- **Automated Ranking**: Instantly sort candidates based on a weighted compatibility score.
- **Skill Mapping**: Visualize matched and missing skills with intuitive, color-coded badges.
- **Premium PDF Export**: Generate boardroom-ready hiring reports with consistent branding and recruiter insights.
- **Carousel + Table Views**: Visualize results side-by-side or in a sortable table.

### 🛡️ Privacy & Security First
- **Browser-Native**: No server-side storage. All processing happens between your browser and your AI provider.
- **Session Security**: API keys are stored only in volatile session memory and are cleared when the tab is closed.

---

## 🤖 Supported AI Providers

| Provider | Key Required | Model Used | Notes |
|---|---|---|---|
| **Pollinations AI** | ❌ None | `openai` (public) | Default — works instantly |
| **Google Gemini** | ✅ Free | `gemini-2.0-flash` | [Get key](https://aistudio.google.com) |
| **Groq** | ✅ Free | `llama-3.3-70b-versatile` | [Get key](https://console.groq.com) |
| **NVIDIA NIM** | ✅ Free credits | `llama-3.3-70b-instruct` | [Get key](https://build.nvidia.com) |
| **OpenRouter** | ✅ Free | `llama-3.3-70b-instruct:free` | [Get key](https://openrouter.ai) — auto-fallback |
| **OpenAI** | 💳 Paid | `gpt-4o-mini` | New accounts get $5 credit |
| **Anthropic Claude** | 💳 Paid | `claude-sonnet-4` | Industry-leading quality |

---

## 📖 Quick Start Guide

1. **Open the App**: Access the [Live Demo](https://resumeiq-compare-jd.netlify.app/) or open `index.html` locally.
2. **Setup Provider**: Click the **"Click to set AI Provider"** pill in the nav bar and enter your API key.
3. **Define the Role**: Paste the Job Description into the JD field.
4. **Upload Resumes**: Drag and drop resumes into the drop zone.
5. **Analyze**: Click **"Analyze Candidates"** and watch the AI rank them in real-time.
6. **Chat & Export**: Use the Chat Bubble for follow-up questions, then export to PDF.

---

## 🔑 How to Get a Free API Key

### Google Gemini (Recommended)
1. Visit [aistudio.google.com](https://aistudio.google.com) and sign in.
2. Click **"Get API Key"** → **"Create API key"**.

### Groq (Fastest)
1. Visit [console.groq.com](https://console.groq.com) and sign up.
2. Go to **"API Keys"** → **"Create API Key"**.

---

## 📄 How It Works

```
Upload Resumes (PDF/DOCX/TXT)
        ↓
Extract Text (PDF.js for PDFs, FileReader for others)
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
| **Logic** | Vanilla JavaScript (ES6+) — Zero Dependencies |
| **PDF Parsing** | [PDF.js](https://mozilla.github.io/pdf.js/) via CDN |
| **Typography** | Playfair Display (Headings) & Outfit (UI/Body) |

---

## 📁 Repository Structure

```
resumeIQ/
├── resume-analyzer.html   # The entire application (single file)
├── README.md
└── LICENSE
```

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

**Built with precision by [opsengine-sys](https://github.com/opsengine-sys)**. *All rights reserved.*
