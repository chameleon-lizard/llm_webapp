# LLM Web App

Simple single-page chat application for talking to LLM APIs directly from your browser.

## Features

- 💬 Multiturn dialogue with conversation history
- 📎 File attachments (automatically converted to text and added to prompts)
- 🔧 Configurable API endpoint and model
- 🔑 Optional API key (works with local LLMs without authentication)
- 💾 Settings saved in browser localStorage
- 📱 Mobile-friendly responsive design

## Usage

### Option 1: GitHub Pages (Recommended)

Open: **https://chameleon-lizard.github.io/llm_webapp/chat.html**

### Option 2: Download and Open Locally

1. Download `chat.html`
2. Serve it via HTTP:
   ```bash
   python3 -m http.server 8000
   ```
3. Open http://localhost:8000/chat.html

### Configuration

1. Set your API endpoint (e.g., `http://localhost:11434/v1/chat/completions` for Ollama)
2. Add API key if required (optional for local endpoints)
3. Set model name
4. Start chatting!

## Compatible APIs

Works with any OpenAI-compatible API:
- OpenAI
- Anthropic (with adapter)
- Local LLMs: Ollama, LM Studio, llama.cpp server
- Any OpenAI-compatible endpoint

## Local LLM Setup

For Ollama, enable CORS:
```bash
export OLLAMA_ORIGINS="*"
ollama serve
```

Then use endpoint: `http://localhost:11434/v1/chat/completions`

## License

MIT
