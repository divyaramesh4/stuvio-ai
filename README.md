

```md
# Stuvio AI: Interactive Educational Video & Quiz Generator

---

## 📌 Project Overview

**Stuvio AI** is a web application that enhances learning by generating short educational videos and interactive quizzes using AI. It converts text into engaging multimedia content to provide a structured and interactive learning experience.

---

## ✨ Features

- 📚 **Topic-Based Content Generation**  
  Enter any topic, and the app generates educational content using AI.

- 🎥 **Video Creation**  
  Synthesizes speech and overlays it on a background to produce short videos.

- 📝 **Interactive Quizzes**  
  Automatically generates MCQs based on the provided topic.

- 💻 **Dynamic UI**  
  Responsive and user-friendly interface for easy interaction.

---

## 🛠️ Technologies Used

| Layer       | Tech Stack                         |
|-------------|------------------------------------|
| Backend     | Flask (Python Web Framework)       |
| AI API      | Google Gemini API                  |
| TTS         | gTTS (Google Text-to-Speech)       |
| Video       | moviepy (Python video editor)      |
| Frontend    | HTML, CSS, JavaScript              |
| Env Mgmt    | Python `venv`, `pip`               |

---

## 📁 Project Structure

```

stuvio\_project/
│
├── ai\_video.py            # Core AI and video logic
├── index.py               # Flask server entry point
│
├── static/                # Static files
│   ├── style.css
│   ├── script.js
│   ├── background.jpg
│   └── output.mp4         # Generated video
│
├── templates/             # HTML templates
│   ├── index.html
│   ├── video\_page.html
│   └── quiz\_page.html
│
├── .env                   # API keys & secrets (not committed)
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation

````

---

## 🧩 Setup and Local Installation

### ✅ Prerequisites

- Python 3.8+
- pip
- FFmpeg (Required for `moviepy`)

### 🔧 FFmpeg Installation

- **Windows**: Download from [ffmpeg.org](https://ffmpeg.org) → extract → add `/bin` to PATH  
- **macOS**:  
  ```bash
  brew install ffmpeg
````

* **Linux**:

  ```bash
  sudo apt update && sudo apt install ffmpeg
  ```

---

### ⚙️ Installation Steps

1. **Clone or open your project folder**

   ```bash
   git clone <your-repo-url>
   cd stuvio_project
   ```

   *Or manually navigate to:*

   ```bash
   cd C:\Users\divya\Downloads\Documents\project
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   ```

   * **PowerShell**: `.\venv\Scripts\Activate.ps1`
   * **CMD**: `venv\Scripts\activate.bat`
   * **Linux/macOS**: `source venv/bin/activate`

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**

   Create a `.env` file with:

   ```
   GEMINI_API_KEY="your_actual_gemini_api_key"
   FLASK_SECRET_KEY="your_secret_key_here"
   ```

---

## 🚀 Running the Application

Start the Flask server:

```bash
python api/index.py
```

Open in browser: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🧪 Usage Guide

1. Enter a **topic** in the homepage input field.
2. Click **Generate Video** or **Generate Quiz**.
3. Wait for processing.
4. View the results on the respective output page.

---

## ⚠️ Notes

* Video generation may take time depending on input length.
* Ensure FFmpeg is installed and added to system `PATH`.
* Check the terminal for Flask logs if you encounter errors.
* Monitor Google Gemini API usage to avoid overages.

---

```


