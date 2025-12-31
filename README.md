# LLM Web App

Simple single-page chat application for talking to LLM APIs directly from your browser.

## Features

- 💬 Multiturn dialogue with conversation history
- 📎 File attachments (automatically converted to text and added to prompts)
- 🔧 Configurable API endpoint and model
- 🔑 Optional API key (works with local LLMs without authentication)
- 💾 Settings saved in browser localStorage
- 📱 Mobile-friendly responsive design
- ⚙️ Advanced settings:
  - System prompt (with JSON file import)
  - Inference parameters (temperature, top_p, repetition_penalty, do_sample)
  - Streaming responses (real-time token-by-token generation)
- 📝 Rich text rendering:
  - Full Markdown support (headers, lists, tables, links, images, etc.)
  - LaTeX math formulas (inline with `$...$` and display with `$$...$$`)
  - Syntax highlighting for code blocks
  - GitHub Flavored Markdown (GFM)

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
4. (Optional) Configure advanced settings:
   - Click "Advanced Settings" to expand
   - Set system prompt (or load from JSON file)
   - Adjust inference parameters
5. Start chatting!

### Advanced Settings

#### System Prompt

You can set a system prompt directly in the textarea or load it from a JSON file with the following structure:

```json
{
    "content": "Your system prompt here"
}
```

Example file is provided in `system_prompt_example.json`.

#### Inference Parameters

Default values:
- **Temperature**: 0.7 (controls randomness, 0-2)
- **Top P**: 0.3 (nucleus sampling threshold, 0-1)
- **Repetition Penalty**: 1.1 (penalizes repetition, 1-2)
- **Do Sample**: enabled (enables sampling instead of greedy decoding)
- **Stream Response**: enabled (receive responses token-by-token in real-time)

**Note**: Streaming requires the API endpoint to support Server-Sent Events (SSE). Most OpenAI-compatible APIs support this feature.

### Markdown and Math Support

The app supports full Markdown rendering in messages:

#### Text Formatting
- **Bold**: `**text**` or `__text__`
- *Italic*: `*text*` or `_text_`
- `Inline code`: `` `code` ``
- ~~Strikethrough~~: `~~text~~`

#### Headers
```markdown
# H1
## H2
### H3
```

#### Lists
```markdown
- Unordered item
- Another item

1. Ordered item
2. Another item
```

#### Code Blocks
````markdown
```python
def hello():
    print("Hello, World!")
```
````

#### Math Formulas

Inline math: `$E = mc^2$` renders as $E = mc^2$

Display math:
```
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$
```

#### Tables
```markdown
| Column 1 | Column 2 |
|----------|----------|
| Cell 1   | Cell 2   |
```

#### Other Elements
- Links: `[text](url)`
- Images: `![alt](url)`
- Blockquotes: `> quote`
- Horizontal rule: `---`

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
