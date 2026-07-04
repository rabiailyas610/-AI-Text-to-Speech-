<div align="center">
  <h1>🎙️ Agentic TTS Pro</h1>
  <p><strong>AI-Powered Text-to-Speech with Gemini Emotion Detection</strong></p>
  <p>
    <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
    <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white" alt="Gemini">
    <img src="https://img.shields.io/badge/Edge_TTS-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" alt="Edge TTS">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License">
  </p>
</div>

## 📖 Overview

**Agentic TTS Pro** is an intelligent text-to-speech system that uses **Google Gemini** to detect the emotion and tone of the input text, and then generates speech with **automatically adjusted speed and pitch** using **Microsoft Edge TTS**.

Unlike traditional TTS apps where users manually adjust sliders, this system **autonomously** decides the speech parameters based on the emotional context of the text.

## 🚀 Features

| Feature | Description |
| :--- | :--- |
| 🧠 **Emotion Detection** | Gemini AI analyzes text tone — Happy, Sad, Angry, Neutral, Professional, Excited |
| 🎙️ **Expressive TTS** | Edge TTS generates speech with AI-adjusted speed and pitch based on detected emotion |
| 💾 **Persistent History** | All conversions saved with audio files in JSON + MP3 format |
| 🔊 **Audio Replay** | Re-listen to any past conversion directly from history |
| 🗑️ **Individual Delete** | Delete specific history entries (audio file removed as well) |
| 📥 **Download MP3** | Download speech files for offline use |
| 📱 **Mobile Responsive** | Optimized for both desktop and mobile devices |

## 🧠 How It Works (Agentic Flow)

```
┌─────────────────────────────────────────────────────────────────┐
│                      User Inputs Text                          │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│              🤖 Agent: Gemini AI (Emotion Analysis)            │
│   Detects: Happy, Sad, Angry, Neutral, Professional, Excited   │
│   Outputs: emotion, speed (0.7–1.3), pitch (-30 to +30 Hz)   │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│              🎙️ Edge TTS (Speech Generation)                   │
│   Generates speech with AI-adjusted speed and pitch            │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                   🔊 Audio Output & History                    │
│   Play, Download, or Save to Persistent History               │
└─────────────────────────────────────────────────────────────────┘
```

## 🛠️ Tech Stack

| Category | Technology |
| :--- | :--- |
| **Frontend** | Streamlit |
| **LLM (Emotion Detection)** | Google Gemini (`gemini-2.5-flash`) |
| **TTS Engine** | Microsoft Edge TTS |
| **Storage** | JSON (History) + MP3 (Audio) |
| **Deployment** | Streamlit Community Cloud |

## 📦 Installation

### Prerequisites
- Python 3.10+
- Google Gemini API key ([Get it here](https://aistudio.google.com/))

### Steps

```bash
# Clone the repository
git clone https://github.com/rabiailyas610/agentic-tts-system.git
cd agentic-tts-system

# Create virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
echo "GOOGLE_API_KEY=your_api_key_here" > .env

# Run the application
streamlit run app.py
```

## 📁 Project Structure

```
agentic-tts-system/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (API keys)
├── tts_history.json       # Persistent history (auto-generated)
├── history_audio/         # Audio files (auto-generated)
└── README.md              # This file
```

## 🧪 Example Inputs & AI Decisions

| User Input | Detected Emotion | AI Speed | AI Pitch |
| :--- | :--- | :--- | :--- |
| *"Congratulations on your promotion!"* | Happy | 1.15x | +25 Hz |
| *"I feel so sad and lonely..."* | Sad | 0.80x | -20 Hz |
| *"This is completely unacceptable!"* | Angry | 1.30x | +35 Hz |
| *"Thank you for your consideration."* | Professional | 1.00x | 0 Hz |
| *"Oh my god, we did it!"* | Excited | 1.40x | +30 Hz |

## 🎯 Key Engineering Decisions

1. **Gemini over Rule-Based Detection**: Gemini understands nuanced emotions (sarcasm, subtle excitement) better than simple keyword matching.

2. **Edge TTS over Azure/Google TTS**: Edge TTS is free, has natural voices, and supports speed/pitch adjustment without API costs.

3. **Persistent History**: JSON + MP3 files ensure history survives app restarts and can be backed up.

4. **Individual Delete**: Each history entry has a unique ID, allowing precise control without deleting everything.

5. **Agentic Approach**: The system autonomously decides speech parameters — user doesn't need to adjust sliders manually.

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Google Gemini for emotion analysis
- Microsoft Edge TTS for speech synthesis
- Streamlit for the amazing UI framework

## 📬 Contact

**Rabia Ilyas**  
[GitHub](https://github.com/rabiailyas610) | [LinkedIn](https://www.linkedin.com/in/rabia-ilyas-37436131a)


<div align="center">
  ⭐ If you found this project useful, please star the repository! ⭐
</div>
