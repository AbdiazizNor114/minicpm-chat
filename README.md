# Local AI Helper — MiniCPM5-1B

A clean, minimal chat interface for getting a little help from **MiniCPM5-1B** on your own machine through Ollama. No API keys, no cloud account, and no usage cost.

![Local AI Chat UI](https://img.shields.io/badge/runs-100%25%20locally-1D9E75?style=flat-square) ![Model](https://img.shields.io/badge/model-MiniCPM5--1B-blue?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-gray?style=flat-square)

---

## Features

- **Local AI help** — powered by [Ollama](https://ollama.com) on your machine
- **Streaming responses** — text appears word by word as the model generates
- **Markdown rendering** — bold, lists, headings all rendered properly
- **Syntax highlighted code** — with a one-click Copy button
- **Table rendering** — clean formatted tables from model output
- **LaTeX math** — equations rendered via MathJax
- **Dark mode** — automatically follows your system preference
- **No build step** — plain HTML, CSS, and JavaScript files you can open in a browser

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

Open `index.html` in your browser. That's it.

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
├── index.html                  # Main app entry point to open in the browser
├── styles.css                  # Responsive layout, theme, chat bubbles, and dark mode
├── app.js                      # Ollama connection, streaming chat, Markdown, copy buttons
├── minicpm-chat.html           # Legacy single-file version kept for reference
├── minicpm-chat.original.html  # Original backup before splitting the app into files
└── README.md                   # Setup notes, feature overview, and project documentation
```

The current app uses the split-file version:

- `index.html` loads the page shell, CDN libraries, stylesheet, and JavaScript.
- `styles.css` owns the visual polish so the markup stays clean.
- `app.js` handles user input, sends chat requests to Ollama, streams responses, and renders Markdown/code/math output.

`minicpm-chat.html` and `minicpm-chat.original.html` are kept as history/reference files. For normal use, open `index.html`.

---

## About

Built by **Abdiaziiz** — AI Engineering student at Dalarna University, Sweden.  
Part of an ongoing series of local AI and ML portfolio projects.

- Portfolio: [aziz.smidify.se](https://aziz.smidify.se)
- GitHub: [@AbdiazizNor114](https://github.com/AbdiazizNor114)

---

## License

MIT — free to use, modify, and build on.
