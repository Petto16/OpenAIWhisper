# OpenAI Whisper Transcriber

This project allows automatic transcription of the audio file `audio.mp3` into text using OpenAI Whisper.

## 📌 Requirements

- **Python 3.8+** (recommended version 3.9 or 3.10)
- **FFmpeg** (required for audio processing)
- **Virtual environment (optional but recommended)**

## 🔧 Installation

### 1️⃣ Clone the Project

```bash
git clone https://github.com/MKovacik/OpenAIWhisper.git
cd OpenAIWhisper
```

### 2️⃣ Create and Activate a Virtual Environment (Recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate    # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Install FFmpeg (If Not Installed)

**macOS (Homebrew):**

```bash
brew install ffmpeg
```

**Ubuntu/Linux:**

```bash
sudo apt update && sudo apt install ffmpeg
```

**Windows:**

- Download `ffmpeg` from [official site](https://ffmpeg.org/download.html)
- Add `ffmpeg` to the system `PATH`

Verify installation:

```bash
ffmpeg -version
```

If you see a version output, everything is fine. ✅

## 🚀 Usage

1. **Place the audio file** `audio.mp3` in the same directory as `whisper_transcriber.py`.
2. **Run the script:**
   ```bash
   python whisper_transcriber.py
   ```
3. **Enter the model size**, e.g., `small`, `medium`, `large` (default: `small`).
4. **Enter the language** for transcription (default: Slovak). Examples:
   - **English:** `english`
   - **German:** `german`
   - **French:** `french`
5. **The output transcription** is saved to `audio_transcript.txt`.

## 🛠 Troubleshooting

**Error:** `FileNotFoundError: [Errno 2] No such file or directory: 'ffmpeg'`

- Ensure `ffmpeg` is installed (`ffmpeg -version`).
- If the error persists, add `ffmpeg` to the `PATH` or reinstall it.

**Model downloads every time I run the script**

- Models are stored by default in `~/.cache/whisper/`.
- To store models locally, the script uses the `models/` folder.

## 📂 Project Structure

```
whisper-transcriber/
├── whisper_transcriber.py  # Main script
├── requirements.txt        # Python dependencies
├── README.md               # Documentation
├── models/                 # Stores Whisper models
│   ├── small.pt            # (Example model)
├── audio.mp3               # Audio file for transcription
├── audio_transcript.txt    # Output text file
```

## 🎯 License

This project is available under the MIT license.

---

For any issues or questions, open an issue on GitHub! 🚀

