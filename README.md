# Log-Viewer

A web app for reading and analyzing local `.log` files — with an integrated AI assistant for debugging errors.

Upload your `.log` file, search and filter through entries, and let AI explain errors and suggest fixes on the spot.

---

## AI Features

### AI Fix Assistant

Every error or warning line in the log viewer has a **✨ Fix** button. Clicking it opens a side panel where the AI:

1. Explains what the error means
2. Identifies the likely cause
3. Suggests a concrete fix

The AI receives the error line plus 5 lines of surrounding context for accurate, relevant answers.

After the initial analysis, you can ask follow-up questions in a **chat interface** — the full conversation history is maintained so the AI keeps context across multiple messages.

---

### Supported AI Providers

The app supports five AI providers. You can switch between them at any time:

| Provider | Model |
|---|---|
| **OpenAI** | GPT-4o Mini |
| **Anthropic (Claude)** | Claude Haiku |
| **Google AI** | Gemini 1.5 Flash |
| **Groq** | LLaMA 3.1 8B Instant |
| **Together AI** | Meta LLaMA 3.1 8B Turbo |

Each provider requires its own API key, entered directly in the AI panel. Keys are saved in browser session storage and cleared when the tab is closed.

---

## Usage

1. Open `log_file_analyzer.html` in a browser
2. Upload a `.log` file
3. Hover over any error or warning line — a **✨ Fix** button appears
4. Click **Fix** to open the AI panel
5. Select a provider, enter your API key, and the analysis runs automatically
6. Use the chat input to ask follow-up questions

> No backend required. All API calls are made directly from the browser.
