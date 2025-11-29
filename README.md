# OrthoSnip

OrthoSnip is an **orthopedic EMR documentation assistant**.

It helps clinicians turn messy real-world inputs (screen snips, PDFs, dictation, ROM measurements) into clearer, more structured documentation — while keeping everything **local, clinician-controlled, and no-cloud**.

> **Tagline:**  
> Clinician-led, local-first, no-cloud tools for orthopedic EMR and AI-assisted documentation.

---

## ⚠️ Medical / Safety Notice

OrthoSnip is a **documentation and education assistant only**.

- It does **not** provide medical advice and is **not** a diagnostic or treatment tool.
- It has **not** been reviewed, cleared, or approved by the **FDA**, **EMA**, or any other regulator.
- Any outputs (summaries, physical exam text, suggested wording, ROM descriptions, etc.) must be
  **reviewed, edited, and interpreted by a licensed clinician**.
- Patients and non-clinicians must **not rely on this tool** for medical decisions or emergencies.
- If you use this in a clinical environment, **you are responsible** for complying with all applicable
  laws, regulations, and institutional policies. Do not treat this as a regulated medical device
  unless it has been formally evaluated and cleared under the applicable rules.

---

## Why this project is useful

Older EMR systems and radiology/clinic workflows make it hard to:

- Copy relevant information out of scanned PDFs or clunky EMR screens.
- Clean up raw dictation into clear, readable documentation.
- Quickly build consistent orthopedic physical exam notes.
- Document range of motion (ROM) in a structured way.

OrthoSnip aims to help with all of that by:

- Running on the clinician’s **own Windows machine** (local-first, no cloud).
- Using **local OCR** to turn images/snips/PDF pages into text.
- Using **local LLMs via Ollama** to help structure and polish documentation.
- Providing simple helpers for documenting **joint ROM**.

It is **not** a replacement for clinical judgment, radiology reports, or formal measurements — it is a tool to make note-writing and documentation more efficient.

---

## What you can do with OrthoSnip

Depending on how you configure it, OrthoSnip can:

- 🖼️ **Convert EMR “snips” and PDFs to text**
  - Capture screenshots from your EMR or load images/PDF pages.
  - Use local OCR (e.g., Windows WinRT OCR; optional handwriting/Whisper modules) to extract text.

- 🧠 **Use local LLMs to improve documentation**
  - Clean up dictation text.
  - Turn raw OCR text into structured bullet points.
  - Draft physical exam language based on your inputs and templates.
  - All via **local Ollama models** (no cloud API keys required).

- 🦵 **Assist with range-of-motion (ROM) documentation**
  - Use camera/video helpers (e.g., MediaPipe) for ROM guidance.
  - Or enter ROM values manually and generate consistent narrative text.

All of this is meant to **support the clinician** — not to make autonomous decisions.

---

## How to use it (basic workflow)

### 1. Requirements (typical setup)

- Windows 10 or 11
- Python 3.9 or 3.11 (for running from source)
- [Ollama](https://ollama.com/) installed and running locally
  - You can start with a small general model (e.g., `llama3:8b` or similar).
- Recommended Python packages (exact list may be in `requirements.txt`), for example:
  - `Pillow`
  - `PyMuPDF` (`fitz`)
  - `numpy`
  - Optional: `opencv-python`, `mediapipe`, `whisper`, `rapidfuzz`, etc.

### 2. Run from source (example)

```bash
git clone https://github.com/OrthoSnip/OrthoSnip.git
cd OrthoSnip

# (Optional but recommended)
python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt

# Start the GUI (adjust script name if different)
python OrthoSnip.py
OrthoSnip is released under the OrthoSnip License Agreement (Non-Commercial Use).

You may use OrthoSnip on your own computer for personal, educational, research,
or internal clinical documentation support.

You may not redistribute OrthoSnip, integrate it into commercial EMR systems,
or offer it as a paid or hosted service without a separate commercial license.

All rights are reserved by the author.

See the LICENSE
 file in this repository for the full text.

Commercial use

If you are an EMR vendor, healthcare IT company, or other commercial entity interested in:

integrating OrthoSnip into your product,

distributing it to your customers, or

obtaining support and maintenance,

please contact the author to discuss a commercial license and integration agreement.
