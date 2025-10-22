🎙️ Google Cloud Voice Assistant powered by Gemini 2.5 Flash

> A real-time voice assistant built with **Google Cloud Speech-to-Text**, **Text-to-Speech**, and **Gemini 2.5 Flash**.  
> Record your voice → get instant transcription → AI reply → natural voice playback — all inside one Gradio app.

---

## 🚀 Demo Screenshot

<p align="center">
  <img src="https://cdn.discordapp.com/attachments/1407401653325271080/1430567033807962112/Screenshot_2025-10-22_at_10.42.21_AM.png?ex=68fa3edf&is=68f8ed5f&hm=7724a6cb0252c78dfbc43aea0a535ac848bfe0313cfc0ef28a69a07449e3d2eb&" width="85%">
</p>

---

## ✨ Features

- 🎤 **Speech-to-Text** — high-accuracy transcription using Google Cloud Speech  
- 🧠 **Gemini 2.5 Flash** — ultra-fast generative replies via Google Generative AI  
- 🔊 **Text-to-Speech** — realistic Neural2 voice playback  
- 💬 Instant transcript + AI reply displayed side-by-side  
- 🔁 **Replay / Redo** button to replay last Gemini reply  
- 🧩 Modular Python design — extend for chat memory, translation, or custom voices  
- ⚙️ Works in **Google Colab**, **VS Code**, or any local Python 3.10+ environment  

---

## 🛠️ Installation

### 1️⃣ Clone Repo
```bash
git clone https://github.com/yourusername/voice-assistant-gemini.git
cd voice-assistant-gemini
2️⃣ Install Dependencies
bash
Copy code
pip install google-cloud-speech google-cloud-texttospeech google-generativeai gradio ffmpeg-python --quiet
pip install -U google-generativeai --quiet
🔑 API Setup
A. Google Cloud Credentials
Enable Speech-to-Text and Text-to-Speech APIs in your Google Cloud Console.

Create a Service Account → download its JSON key.

Upload the file to your project directory or Colab.

The app will auto-detect and load it.

B. Gemini API Key
Get a key from Google AI Studio → paste it when prompted.

▶️ Usage
Run in Colab or Locally
bash
Copy code
python voice_assistant_gemini.py
You’ll see:

vbnet
Copy code
⚠️ Please upload your Google Cloud JSON key file
🔑 Enter your Gemini API Key:
✅ Loaded credentials: service-key.json
Then open the Gradio UI → record your voice.

🧠 Workflow
Step	Function	Description
1️⃣	Upload JSON Key	Authenticate Google Cloud Speech + TTS
2️⃣	Enter Gemini API Key	Configures google-generativeai SDK
3️⃣	Record Audio	Audio compressed to 16 kHz mono WAV
4️⃣	Speech-to-Text	Google Cloud Speech recognizes voice
5️⃣	Gemini Reply	models/gemini-2.5-flash generates response
6️⃣	Text-to-Speech	Neural voice MP3 output
7️⃣	Replay Button	Replays last response

💻 UI Preview
vbnet
Copy code
🎙️ Speak to the AI Assistant
-----------------------------------------
[🎤 Speak Now]         (3 sec recording)
🧠 Transcription: what is the value of pi
🤖 Assistant Reply: It's 3.14159 – an irrational number.
🔊 Voice Reply       (plays MP3)
✅ Click Record, speak, and get Gemini’s voice reply back!
🧩 Directory Structure
vbnet
Copy code
voice-assistant-gemini/
├── voice_assistant_gemini.py
├── requirements.txt
├── README.md
└── service-key.json
requirements.txt

txt
Copy code
google-cloud-speech
google-cloud-texttospeech
google-generativeai
gradio
ffmpeg-python
⚠️ Common Errors & Fixes
❌ 404 – Model Not Found
Upgrade your SDK and use:

python
Copy code
model = genai.GenerativeModel("models/gemini-2.5-flash")
❌ 503 – Service Unavailable
Gemini servers may be busy → retry after 10–20 seconds.

⚠️ Mic Replay Button Not Working
Gradio’s mic widget does not auto-trigger callbacks.
Use the 🔁 Replay / Redo button added below the UI.

🧠 Future Improvements
Add chat memory to preserve context

Add language auto-detection + translation

Switch voices dynamically from UI

Enable real-time streaming STT + TTS

Integrate Gemini 2.5 Pro for long context reasoning

🙌 Credits
Google Cloud Speech-to-Text

Google Cloud Text-to-Speech

Google Gemini 2.5 Flash

Gradio Framework

🏁 Quick Start (Summary)
bash
Copy code
pip install google-cloud-speech google-cloud-texttospeech google-generativeai gradio ffmpeg-python -q
python voice_assistant_gemini.py
1️⃣ Upload your Google Cloud key
2️⃣ Enter Gemini API key
3️⃣ Record audio → AI reply → voice output

<p align="center">Made with ❤️ by Abhishek Vijay Bote</p> ```
