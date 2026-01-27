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
```


---
# 🧠 LLM with Smart Long-Term Memory (Mistral 7B + FAISS)

A minimal **LLM chat system with selective long-term memory**, built using
**Mistral-7B**, **LangChain**, and **FAISS**, runnable on a **FREE Google Colab GPU**.

Instead of storing every message, this project uses the LLM itself to decide  
**what is worth remembering long-term**.

---

## ✨ Features

- 🧠 Short-term memory via `ConversationSummaryMemory`
- 🗂️ Persistent long-term memory with **FAISS**
- ⚖️ LLM-based importance filtering (store only useful memories)
- 🔎 Semantic retrieval of relevant past interactions
- ⚡ 4-bit quantized Mistral-7B (low VRAM)
- 🎛️ Simple Gradio chat UI

---

## 🧩 Memory Design

This system uses **three memory layers**:

1. **Summary Memory**
   - Compresses recent conversation
   - Prevents context window overflow

2. **Vector Memory (FAISS)**
   - Stores important interactions only
   - Persists on disk

3. **Importance Filter**
   - The LLM decides whether an interaction is worth saving
   - Avoids memory pollution

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Mistral-7B-Instruct
- LangChain (classic + community)
- FAISS
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
langchain langchain-community sentence-transformers faiss-cpu
```
4.Run the script

5.Open the generated Gradio share link

---
# 🧠 LLM Smart Memory Agent

A minimal **LLM chat system with structured, selective, multi-user memory**.
Built using **Mistral-7B**, **LangChain**, and **FAISS**, and runnable on a
**FREE Google Colab GPU**.

The focus of this project is **memory architecture**, not prompt tricks.

---

## ✨ Features

- 🧠 Short-term context via `ConversationSummaryMemory`
- 🗂️ Persistent long-term memory with FAISS
- ⚖️ LLM-based importance scoring (0–10)
- 🏷️ Memory classification (fact / preference / ignore)
- 👥 Multi-user memory isolation
- 🔎 Semantic memory retrieval
- ⚡ 4-bit quantized Mistral-7B
- 🎛️ Simple Gradio chat UI

---

## 🧩 Memory Design

Each interaction is processed as follows:

1. Retrieve relevant memories (FAISS)
2. Inject memories into the prompt
3. Generate response using summary memory
4. Ask the LLM:
5. Score importance (0–10)
6. Classify memory type:
- `fact`
- `preference`
- `ignore`
7. Persist only useful memories

---

## 🗂️ Memory Structure

```text
memory_store/
└── user_id/
  ├── facts/
  └── preferences/
```
---
# 🧠 LLM Custom Agent with Decaying Memory & Tools

A **custom-built LLM agent** with manual routing, tool usage, and
**long-term memory with importance decay**, running on a **FREE Google Colab GPU**.

This project avoids LangChain agents and instead implements
**explicit control over routing, memory, and tools**.

---

## ✨ Features

- 🤖 Manual router (LLM decides what to do)
- 🧮 Calculator tool
- 🧠 Short-term context via `ConversationSummaryMemory`
- 🗂️ Persistent long-term memory with FAISS
- ⚖️ LLM-based importance scoring (0–10)
- ⏳ Memory decay over time (exponential decay)
- 👥 Multi-user memory isolation
- ⚡ 4-bit quantized Mistral-7B (NF4)
- 🎛️ Gradio chat UI

---

## 🧩 Agent Design

This agent does **not** rely on built-in agent abstractions.

Instead, it uses:
- explicit routing logic
- custom tools
- manual memory control

### Routing Logic

For each user message, the LLM chooses one route:

- `calculator` → math expressions
- `memory` → summarize stored memories
- `chat` → normal conversation

---

## 🧠 Memory System

Each interaction is processed as follows:

1. Retrieve relevant memories from FAISS
2. Rank memories using **importance × time decay**
3. Inject top memories into the prompt
4. Generate response
5. Score interaction importance (0–10)
6. Store only important memories
7. Apply decay over time

### Memory Decay Formula

score = importance * e^(-λ × age_in_days)


This prevents old or irrelevant memories from dominating context.

---

## 🗂️ Memory Structure

```text
memory_store/
 └── user_id/
     └── facts/
```
Each user has isolated memory

Memories persist across sessions

Stored with metadata (importance + timestamp)
