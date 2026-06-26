# 🎙️ Personal Storyteller with Llama & gTTS

> Generate engaging, educational stories with AI and hear them read aloud — all in a Jupyter notebook.

---

## Overview

This project combines **Meta's Llama** (a powerful open-source LLM) with **gTTS** (Google Text-to-Speech) to build a personal storytelling assistant. You provide a topic, the AI crafts a clear and engaging story, and then the story is converted to natural-sounding audio you can play right in your notebook.

Whether you want a bedtime story, an educational explainer, or a fun way to learn about any subject — this pipeline has you covered.

---

## What It Does

1. **Generates a story** — Uses Llama via the Hugging Face Inference API to write a 200–300 word educational story on any topic you choose.
2. **Converts text to speech** — Passes the story through gTTS to produce natural-sounding audio.
3. **Plays audio in-notebook** — Renders an audio widget directly inside Jupyter for instant playback.
4. **Optionally saves the audio** — Export the story as an `.mp3` file.

**Example:** Input `"the life cycle of butterflies"` → get a friendly narrative + audio explanation, perfect for beginners.

---

## Tech Stack

| Component | Purpose |
|---|---|
| [Meta Llama](https://ai.meta.com/llama/) | Story generation via open-source LLM |
| [Hugging Face Inference API](https://huggingface.co/inference-api) | Hosted inference endpoint for Llama models |
| [gTTS](https://gtts.readthedocs.io/) | Google Text-to-Speech for audio conversion |
| [IPython](https://ipython.org/) | In-notebook audio playback widget |
| Jupyter Notebook | Interactive development environment |

---

## Prerequisites

- Python 3.8+
- A Jupyter Notebook environment
- A [Hugging Face account](https://huggingface.co/join) with an API token (free)
- Access approved for a Llama model (e.g. `meta-llama/Llama-3.2-3B-Instruct`) on Hugging Face

---

## Installation

```bash
pip install gTTS==2.5.4
pip install huggingface_hub
```

---

## Setup

1. Get your Hugging Face token from [hf.co/settings/tokens](https://huggingface.co/settings/tokens)
2. Request access to a Llama model on its Hugging Face model page (one-time, approved quickly)
3. Set your token as an environment variable:

```bash
export HF_TOKEN="hf_your_token_here"
```

Or set it inside the notebook:

```python
import os
os.environ["HF_TOKEN"] = "hf_your_token_here"
```

---

## Project Structure

```
.
├── storyteller.ipynb          # Main notebook
├── requirements.txt           # Python dependencies
└── generated_story.mp3        # (Optional) Exported audio output
```

---

## requirements.txt

```
gTTS==2.5.4
huggingface_hub
```

---

## Recommended Llama Models

| Model | Size | Notes |
|---|---|---|
| `meta-llama/Llama-3.2-3B-Instruct` | 3B | Fast, great for storytelling |
| `meta-llama/Llama-3.2-1B-Instruct` | 1B | Lightweight, quickest response |
| `meta-llama/Llama-3.3-70B-Instruct` | 70B | Highest quality, slower |

---

## Learning Objectives

After completing this project, you will be able to:

- Use Llama models via the Hugging Face Inference API to generate creative stories
- Convert generated text to speech using the gTTS library
- Build an end-to-end AI storytelling pipeline
- Play generated audio directly within a Jupyter notebook

---

## Exercises

**Exercise 1:** Generate a story about `"the life cycle of a human"` and convert it to speech.

**Exercise 2:** Try switching to a different Llama model and compare the output quality.

---

## License

This project is open source. Llama models are subject to [Meta's Llama Community License](https://ai.meta.com/llama/license/).
