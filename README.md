# TechCorp IT Support Chatbot (LangChain + Ollama)

A practical project that builds an internal IT support chatbot for routine employee issues (password reset, VPN, email setup, software install help) using LangChain memory and a local Ollama model.

## Features

- Company-specific prompt template with clear escalation boundaries
- Conversation memory across turns with `RunnableWithMessageHistory`
- Local LLM inference with Ollama (no cloud API key required)
- Basic performance tracking:
  - total conversations
  - issues resolved by AI
  - escalations to human IT
- Notebook-based demo with realistic support scenarios

## Project Files

- `TechCorp_IT_Chatbot.ipynb`: main implementation and demo
- `requirements.txt`: Python dependencies
- `.gitignore`: project ignores for Python/Jupyter workflow

## Prerequisites

- Python 3.11+
- Ollama installed: https://ollama.ai/download
- Local model pulled (example):

```bash
ollama pull llama3.2
```

- Ollama running:

```bash
ollama serve
```

## Setup

1. Create and activate a virtual environment.

```bash
python -m venv .venv
.venv\Scripts\activate
```

2. Install dependencies.

```bash
pip install -r requirements.txt
```

3. Launch Jupyter and open the notebook.

```bash
jupyter notebook
```

## How To Run

1. Open `TechCorp_IT_Chatbot.ipynb`.
2. Run cells in order from top to bottom.
3. Review test outputs and performance stats.
4. Use the interactive demo section to try custom IT questions.

## Notes

- The project is designed for local execution and learning.
- Escalation detection combines response cues and critical issue keywords.
- You can swap models by changing the model name in the chatbot class.

## Possible Next Enhancements

- Ticketing system integration
- Knowledge base retrieval for policy/troubleshooting answers
- Sentiment detection for frustration-aware escalation
- Feedback loop to improve answer quality over time
