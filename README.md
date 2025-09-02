
---

# VibeVoiceTTS 🎙️
<img width="1489" height="1217" alt="Screenshot 2025-09-02 213147" src="https://github.com/user-attachments/assets/c9aed0db-8266-444d-8f20-371a870e8d50" />

**Long-form Multi-Speaker Text-to-Speech with Streaming Support**

VibeVoiceTTS is an advanced **AI-powered dialogue & podcast generator** that can create long-form, natural-sounding multi-speaker audio. It features:

* 🎛️ **Configurable podcast generation** (1–4 speakers)
* 🎭 **Custom voices** via audio uploads
* ⚡ **Streaming TTS** (hear audio as it’s being generated)
* 📥 **Easy model management & downloads** (via Hugging Face Hub)
* 🎨 **Beautiful Gradio UI** with light/dark mode

---

## 🚀 Features

* **Multiple speakers** — assign different voices to participants in a conversation.
* **Custom voice cloning** — upload short audio samples (3–30s recommended).
* **Live streaming** — hear speech generation in real-time.
* **Complete audio export** — download finished podcasts.
* **Model management** — download, load, unload, or switch between models.
* **Attention optimization** — choose between Flash Attention 2 or SDPA.
* **Example scripts** — start quickly with preloaded conversations.

---

## 📦 Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/SUP3RMASS1VE/VibeVoiceTTS.git
cd VibeVoiceTTS
python -m venv .venv
.venv\Scripts\activate
pip install uv
uv pip install torch==2.7.0 torchvision torchaudio --index-url https://download.pytorch.org/whl/cu128
uv pip install triton-windows
uv pip install https://github.com/petermg/flash_attn_windows/releases/download/01/flash_attn-2.7.4.post1+cu128.torch270-cp310-cp310-win_amd64.whl
uv pip install -e .

```

---

## 🔧 Usage

### Run the Gradio demo

```bash
python demo/gradio_demo.py
```

This will launch a local Gradio UI in your browser.

### Models

You can download and use pre-trained models directly from the gradio ui:

* **VibeVoice-1.5B** (\~2.7B params) — compact, fast, good for most use cases.
* **VibeVoice-Large** (\~9.3B params) — higher quality, slower (\~45 min generation).

Models are automatically saved under `./models/` unless you specify a custom path.

---

## 🎤 Custom Voices

You can upload your own audio clips (WAV, MP3, FLAC, OGG, M4A, AAC).

* **Length**: 3–30 seconds recommended
* **Content**: Clear, natural speech
* **Quality**: Minimal background noise

Custom voices are saved in the `voices/` directory and appear in the speaker dropdown menu.

---

## 📚 Example Scripts

Example conversations are available in `text_examples/`.
They will automatically show up in the Gradio demo.

---

## ⚙️ Advanced Settings

* **CFG Scale** — controls adherence to the input text.
* **Attention Implementation** — toggle between *Flash Attention 2* (faster, memory efficient) and *SDPA* (fallback).
* **Custom Model Path** — load models from any directory.

---

## 🛑 Risks & Limitations

* May produce **unexpected or biased outputs**.
* Potential for misuse in **deepfakes or disinformation**.
* Generation may take a long time (up to \~90 minutes depending on model).

Users are responsible for ensuring safe and ethical use of generated audio.

---

## 📜 License

[MIT License](LICENSE)

---
