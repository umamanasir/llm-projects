This is a copy of exercises from Ed Donner's AI Engineering course, kept here for my own tracking/reference (not the original course repo).

## Contents

| Notebook | Description |
|---|---|
| `day1_gemini_pm_assistant.ipynb` | Uses Google's **Gemini** model (via the OpenAI-compatible endpoint) to act as an AI project management assistant — takes a project status/task description and drafts a stakeholder update with mitigation options. |
| `ollama_local_summarizer.ipynb` | Runs **Llama 3.2 locally via Ollama** to generate a humorous summary of a scraped website's content. |

> Rename the files above to match whatever they're actually called in this repo.

## Setup

### 1. Environment

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install openai python-dotenv ipython
```

### 2. Gemini notebook

- Create a `.env` file in the repo root with:

GOOGLE_API_KEY=your_key_here

- The notebook calls Gemini through OpenAI's client library, pointed at Google's OpenAI-compatible endpoint (`https://generativelanguage.googleapis.com/v1beta/openai/`), using the `gemini-3.1-flash-lite` model.

### 3. Ollama notebook

- Install [Ollama](https://ollama.com) and make sure it's running locally.
- Pull the model used in the notebook:

```bash
  ollama pull llama3.2
```
- No API key is needed; Ollama is called locally at `http://localhost:11434/v1` via the OpenAI-compatible client.

## Usage

Open either notebook in Jupyter and run the cells top to bottom:

```bash
jupyter notebook
```

## Notes

- These are learning exercises duplicated for personal tracking — not the original course source.
- Swap in your own prompts, models, or target websites to experiment further.
