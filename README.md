# 🩺 AI Doctor with Vision and Voice

An experimental multimodal AI assistant that acts like a **virtual doctor** — capable of analyzing **images of any body part**, understanding **spoken symptoms**, and responding in **natural spoken language**.

This project explores the potential of combining **LLMs**, **Computer Vision**, and **Speech Interfaces** to deliver **accessible AI healthcare interactions**.

---

## 🚀 Features

✅ Upload any body part image (e.g., face, skin, wound, eye, etc.)  
✅ Speak your symptoms using a microphone  
✅ Get a concise, human-style spoken diagnosis  
✅ Two voice synthesis options: **gTTS** (Google) & **ElevenLabs**  
✅ Modular code structure  
✅ Built with **Groq’s Multimodal LLM** + **Whisper STT**

---

## 🧠 Modules Overview

### 1. `brain_of_doctor.py`  
- Uses Groq’s multimodal LLM to analyze the uploaded image + text prompt.
- Model: `meta-llama/llama-4-scout-17b-16e-instruct`

### 2. `voice_of_patient.py`  
- Records the patient's voice using `speech_recognition` and microphone.
- Transcribes audio using Groq's Whisper STT (`whisper-large-v3`).

### 3. `voice_of_doctor.py`  
- Converts text response into voice using:
  - `gTTS` (free, offline)
  - or `ElevenLabs` (realistic voice via API)

### 4. `gradio_app.py`  
- Gradio interface for image upload + voice input
- Shows transcription, doctor's text reply, and audio output

---

## 🛠️ Tech Stack

| Component          | Tech/Library        |
|--------------------|---------------------|
| UI                 | Gradio              |
| LLM (Multimodal)   | Groq + Meta-LLaMA   |
| STT (Speech → Text)| Groq Whisper        |
| TTS (Text → Speech)| gTTS, ElevenLabs    |
| Audio Recording    | SpeechRecognition   |
| Backend Language   | Python              |
| Env Management     | `python-dotenv`     |

---

## 🖼️ Sample Workflow

1. Upload a photo of a visible symptom.
2. Speak your symptoms or complaints via mic.
3. The AI analyzes both and gives a spoken reply like a human doctor.

---

## ⚙️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/faryasir07/AI_DOCTOR_VISION-VOICE.git
cd ai-doctor-vision-voice
```



✅ Step 2: Set Up the Virtual Environment

```bash
python -m venv doctor_venv
source doctor_venv/bin/activate      # Linux/macOS
doctor_venv\Scripts\activate         # Windows
```

✅ Step 3: Install Requirements

```bash
pip install --upgrade pip
pip install -r requirements.txt
```


✅ Step 4: Add Environment Variables
Create a .env file with:

```bash
GROQ_API_KEY=your_groq_api_key
ELEVEN_API_KEY=your_elevenlabs_api_key
```

✅ Step 5: Launch the App

```bash
python gradio_app.py
📸 UI Preview
Uploading Soon: Screenshots or demo video
```


🔮 Roadmap
 1)Add multilingual transcription + response

 2)Integrate a medical symptom database

 3)Mobile compatibility (via Gradio Spaces or Flutter frontend)

 4)Store session logs for learning/tracking

 5)Add more realistic doctor voice emotions using ElevenLabs styles

🤝 Contributing
Contributions, feature requests, and feedback are welcome!

1)Fork the repository

2)Create your feature branch (git checkout -b feature/awesome-feature)

3)Commit your changes (git commit -m 'Add some feature')

4)Push to the branch (git push origin feature/awesome-feature)

5)Open a Pull Request

