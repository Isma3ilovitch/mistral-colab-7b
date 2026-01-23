### mistral-colab-7b
A simple and efficient script to run Mistral-7B-Instruct-v0.2 locally using Hugging Face Transformers. This implementation utilizes 4-bit quantization via bitsandbytes to significantly reduce memory usage, allowing the model to run on consumer-grade GPUs (like Google Colab or local RTX cards).

### Mistral 7B + Gradio running in Google Colab with 4-bit quantization
This code demonstrates how to run the Mistral-7B-Instruct-v0.2 model efficiently on Google Colab using 4-bit quantization. It includes scripts for both a basic text generation example and an interactive Gradio chat interface, allowing users to easily chat with the 7-billion-parameter model on a free GPU without needing high-end hardware.

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
