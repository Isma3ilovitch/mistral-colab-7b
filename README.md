### mistral-colab-7b
A simple and efficient script to run Mistral-7B-Instruct-v0.2 locally using Hugging Face Transformers. This implementation utilizes 4-bit quantization via bitsandbytes to significantly reduce memory usage, allowing the model to run on consumer-grade GPUs (like Google Colab or local RTX cards).
---

### Mistral 7B + Gradio running in Google Colab with 4-bit quantization
This code demonstrates how to run the Mistral-7B-Instruct-v0.2 model efficiently on Google Colab using 4-bit quantization. It includes scripts for both a basic text generation example and an interactive Gradio chat interface, allowing users to easily chat with the 7-billion-parameter model on a free GPU without needing high-end hardware.
---
### 🧠 Mistral Chat with Memory (7B)

A simple **open-source chat application** powered by **Mistral-7B-Instruct**, featuring
conversation **memory**, **4-bit quantization**, and a **Gradio UI** — all runnable on a
**FREE Google Colab GPU**.

This project is designed for learning and experimentation with real LLM systems.

---

## ✨ Features

- 🧠 Short-term conversation memory (last N turns)
- ⚡ 4-bit model loading (low VRAM usage)
- 🎛️ Clean chat interface with Gradio
- 🚀 Runs on free Google Colab GPU
- 🔓 Fully open-source and easy to modify

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Mistral-7B-Instruct
- Gradio
- BitsAndBytes (4-bit quantization)

---

## 🚀 Run on Google Colab

1. Open a new **Google Colab** notebook
2. Enable GPU:  
   `Runtime → Change runtime type → GPU`
3. Install dependencies:

```bash
pip install torch transformers gradio bitsandbytes accelerate
```
---

### 🧠 Mistral Hybrid Memory Chat (7B)

An open-source **LLM chat system with real memory** powered by **Mistral-7B**,
combining **summary-based context** and **persistent vector memory** using
LangChain and Chroma — all runnable on a **FREE Google Colab GPU**.

This project demonstrates how modern AI assistants can remember information
across conversations, not just within a single prompt.

---

## ✨ Key Features

- 🧠 **ConversationSummaryMemory** (compressed short-term context)
- 🗂️ **Persistent long-term memory** with Chroma vector database
- 🔎 Semantic memory retrieval using embeddings
- ⚡ 4-bit quantized Mistral 7B (low VRAM)
- 🎛️ Interactive Gradio chat UI
- 💾 Memory persists across sessions

---

## 🧩 Memory Architecture

This system uses **hybrid memory**:

1. **Summary Memory**
   - Keeps conversations short and efficient
   - Prevents context window overflow

2. **Vector Memory (Chroma)**
   - Stores past conversations as embeddings
   - Retrieves relevant memories by similarity
   - Persists on disk

Together, this mimics **human-like long-term memory**.

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Mistral-7B-Instruct
- LangChain (classic + community)
- Chroma Vector Database
- Sentence-Transformers
- Gradio

---

## 🚀 Run on Google Colab

1. Open a new **Google Colab** notebook  
2. Enable GPU:
   `Runtime → Change runtime type → GPU`

3. Install dependencies:

```bash
pip install torch transformers gradio accelerate bitsandbytes \
langchain langchain-community sentence-transformers chromadb

