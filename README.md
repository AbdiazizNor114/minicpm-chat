# Local AI Chat — MiniCPM5-1B

A clean, minimal chat interface for running **MiniCPM5-1B** entirely on your own machine via Ollama. No API keys. No cloud. No cost. Every token stays on your device.

![Local AI Chat UI](https://img.shields.io/badge/runs-100%25%20locally-1D9E75?style=flat-square) ![Model](https://img.shields.io/badge/model-MiniCPM5--1B-blue?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-gray?style=flat-square)

---

## Features

- **100% local** — powered by [Ollama](https://ollama.com), no data ever leaves your machine
- **Streaming responses** — text appears word by word as the model generates
- **Markdown rendering** — bold, lists, headings all rendered properly
- **Syntax highlighted code** — with a one-click Copy button
- **Table rendering** — clean formatted tables from model output
- **LaTeX math** — equations rendered via MathJax
- **Dark mode** — automatically follows your system preference
- **Zero dependencies** — single HTML file, open in any browser

---

## Demo

> Ask it anything — math, code, comparisons, translations.

```
You: Write a Python function that finds all duplicates in a list.
AI:  [streams a clean, highlighted Python response]

You: Compare bubble sort vs merge sort as a table.
AI:  [renders a formatted comparison table]

You: What is 15% of 847? Think step by step.
AI:  [renders LaTeX math equations]
```

---

## Getting Started

### 1. Install Ollama

Download from [ollama.com](https://ollama.com/download) and install it.

### 2. Pull the model

```bash
ollama pull hf.co/openbmb/MiniCPM5-1B-GGUF
```

### 3. Start Ollama with CORS enabled

**macOS / Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```

### 4. Open the UI

Download `minicpm-chat.html` and open it in your browser. That's it.

---

## Why MiniCPM5-1B?

| Property | Value |
|---|---|
| Parameters | 1 Billion |
| Context length | 131,072 tokens |
| Size on disk | ~700 MB |
| License | Apache 2.0 |
| Runs on | CPU, Apple Silicon, Nvidia GPU |

MiniCPM5-1B punches well above its weight for a 1B model — capable of coding, reasoning, math, and multilingual tasks, all while fitting comfortably in memory on consumer hardware.

---

## Tech Stack

- **Model:** [MiniCPM5-1B](https://huggingface.co/openbmb/MiniCPM5-1B) by OpenBMB
- **Runtime:** [Ollama](https://ollama.com) (local LLM server)
- **Markdown:** [marked.js](https://marked.js.org)
- **Syntax highlighting:** [highlight.js](https://highlightjs.org)
- **Math rendering:** [MathJax](https://www.mathjax.org)
- **UI:** Vanilla HTML/CSS/JS — no frameworks, no build step

---

## Project Structure

```
minicpm-chat/
└── minicpm-chat.html   # Everything — UI, styles, and logic in one file
```

---

## About

Built by **Abdiaziiz** — AI Engineering student at Dalarna University, Sweden.  
Part of an ongoing series of local AI and ML portfolio projects.

- Portfolio: [aziz.smidify.se](https://aziz.smidify.se)
- GitHub: [@AbdiazizNor114](https://github.com/AbdiazizNor114)

---

## License

MIT — free to use, modify, and build on.
