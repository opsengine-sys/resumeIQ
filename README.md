# ResumeIQ — AI Resume Compatibility Analyzer

> **A single-file, browser-based AI tool that scores and ranks resumes against a job description — instantly, privately, and for free.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Netlify-00C7B7?style=flat-square&logo=netlify)](https://resumeiq-atsresumecompare.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](./LICENSE)
[![No Install](https://img.shields.io/badge/No%20Install-Open%20in%20Browser-blue?style=flat-square)]()
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-green?style=flat-square)]()

---

## 🌐 Live Demo

👉 **[https://resumeiq-compare-jd.netlify.app/](https://resumeiq-compare-jd.netlify.app/))** — Open, paste, analyze. No signup, no install.

---

## ✨ Features

- **Multi-Resume Analysis** — Upload up to 10 resumes (PDF, DOCX, TXT, RTF, MD) and rank them all at once
- **AI-Powered Scoring** — Each resume is scored across Skills, Experience, Education, and Communication
- **7+ AI Provider Support** — Use your own free API key or the built-in no-key public AI option
- **Smart OpenRouter Fallback** — Automatically cycles through 4 free models if one is overloaded
- **Recruiter Details** — Capture your name and org for the exported report (session-persisted)
- **PDF Report Export** — One-click export of a fully formatted hiring report
- **Carousel + Table Views** — Visualize results side-by-side or in a sortable table
- **Privacy-First** — Everything runs in your browser; no data is sent to any server other than your chosen AI provider

---

## 🚀 Getting Started

No installation, no build step, no server required.

**Option 1 — Use the live app:**
👉 [resumeiq-atsresumecompare.netlify.app](https://resumeiq-atsresumecompare.netlify.app/)

**Option 2 — Run locally:**
1. **[Download `index.html`](./index.html)**
2. Open it in any modern browser (Chrome, Edge, Firefox)
3. Pick an AI provider and paste your API key (or use the free public option)
4. Paste a job description → upload resumes → click **Analyze**

That's it.

---

## 🤖 Supported AI Providers

| Provider | Key Required | Model Used | Notes |
|---|---|---|---|
| **Pollinations AI** | ❌ None | `openai` (public) | Default — works instantly |
| **Google Gemini** | ✅ Free | `gemini-2.0-flash` | [Get key](https://aistudio.google.com) |
| **Groq** | ✅ Free | `llama-3.3-70b-versatile` | [Get key](https://console.groq.com) — fastest |
| **NVIDIA NIM** | ✅ Free credits | `llama-3.3-70b-instruct` | [Get key](https://build.nvidia.com) |
| **OpenRouter** | ✅ Free | `llama-3.3-70b-instruct:free` | [Get key](https://openrouter.ai) — auto-fallback across 4 models |
| **Together AI** | ✅ $1 free | `Llama-3.1-70B-Turbo` | [Get key](https://api.together.ai) |
| **Mistral AI** | ✅ Free trial | `mistral-small-latest` | [Get key](https://console.mistral.ai) |
| **OpenAI** | 💳 Paid | `gpt-4o-mini` | New accounts get $5 credit |
| **Anthropic Claude** | 💳 Paid | `claude-sonnet-4` | Best quality |
| **Custom / Self-hosted** | Optional | Any OpenAI-compatible | Works with Ollama, LM Studio |

---

## 🔑 How to Get a Free API Key

### Google Gemini (Recommended — Generous Free Tier)
1. Visit [aistudio.google.com](https://aistudio.google.com)
2. Sign in with your Google account
3. Click **"Get API Key"** → **"Create API key"**
4. Copy the key (starts with `AIzaSy...`)

### Groq (Fastest Free Option)
1. Visit [console.groq.com](https://console.groq.com)
2. Sign up → click **"API Keys"** → **"Create API Key"**
3. Copy the key (starts with `gsk_...`)

### OpenRouter (Most Flexible — 200+ Models)
1. Visit [openrouter.ai](https://openrouter.ai)
2. Sign up → go to **"Keys"** → click **"Create Key"**
3. Copy the key (starts with `sk-or-...`)
4. Many models have free daily limits; the tool auto-retries on overload

### NVIDIA NIM
1. Visit [build.nvidia.com](https://build.nvidia.com)
2. Sign up → navigate to any model → click **"Get API Key"**
3. Copy the key (starts with `nvapi-...`)

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

The AI is prompted to return a structured JSON object containing:
- Overall match score (0–100)
- Sub-scores: Skills, Experience, Education, Communication
- Matched skills, missing skills, strengths, concerns
- Summary and hiring recommendation (Hire / Consider / Pass)

---

## 🔒 Privacy & Disclaimer

- **No data is stored by this tool.** Your resumes and job description are processed entirely in your browser.
- Resume text is sent **only** to the AI provider you explicitly select and configure.
- The AI provider may retain data per their own privacy policy. Review the policy of your chosen provider before uploading sensitive documents.
- **All analysis scores and recommendations are generated exclusively by the selected AI provider.** This tool acts solely as an interface and does not influence, manipulate, or verify the AI's conclusions.

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Vanilla HTML + CSS + JavaScript (zero dependencies) |
| PDF Parsing | [PDF.js 3.11](https://mozilla.github.io/pdf.js/) via CDN |
| Fonts | Google Fonts — Playfair Display, Outfit, JetBrains Mono |
| AI | User-supplied API key → provider's REST API |

---

## 📁 Repository Structure

```
resumeIQ/
├── index.html             # The entire application (single file)
├── README.md
└── LICENSE
```

---

## 🤝 Contributing

Issues and PRs are welcome. Since this is a single-file app, all changes go into `index.html`.

1. Fork the repo
2. Make your changes in `index.html`
3. Open a PR with a clear description of what you changed and why

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

**Built by [opsengine-sys](https://github.com/opsengine-sys)**
