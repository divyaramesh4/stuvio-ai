
# 🎓 Stuvio AI: Interactive Educational Video & Quiz Generator

---

## 📌 Project Overview

**Stuvio AI** is a **web application** designed to enhance learning by generating **short, informative videos** and **interactive quizzes** on any given topic.  
Leveraging **Artificial Intelligence**, it creates **engaging content**, synthesizes speech, and offers a structured learning experience for students.

---

## ✨ Features

- **📚 Topic-Based Content Generation** – Input a topic and generate relevant educational material.
- **🎥 Video Creation** – Converts the content to speech and merges it with a background image.
- **📝 Interactive Quizzes** – Creates multiple-choice questions to reinforce understanding.
- **💻 Dynamic UI** – Clean, intuitive, and user-friendly interface.

---

## 🛠️ Technologies Used

| Category              | Tools/Frameworks                  |
|-----------------------|-----------------------------------|
| **Backend**           | Flask (Python Web Framework)      |
| **AI Integration**    | Google Gemini API                 |
| **Text-to-Speech**    | gTTS (Google Text-to-Speech)      |
| **Video Processing**  | moviepy                           |
| **Frontend**          | HTML, CSS, JavaScript             |
| **Environment**       | Python `venv` (Virtual Environment) |
| **Dependency Manager**| pip                               |

---

## 📁 Project Structure

```

stuvio\_project/
├── ai\_video.py           # Core logic for content and video generation
├── index.py              # Flask app entry point
├── static/               # CSS, JS, image, and output video
│   ├── style.css
│   ├── script.js
│   ├── background.jpg
│   └── output.mp4        # Generated video output
├── templates/            # HTML files for rendering views
│   ├── index.html
│   ├── video\_page.html
│   └── quiz\_page.html
├── .env                  # API keys and sensitive variables (excluded from Git)
├── requirements.txt      # Project dependencies
└── README.md             # You are here

````

---

## 🧩 Setup and Local Installation

### ✅ Prerequisites

- **Python 3.8+**
- **pip**
- **FFmpeg** (used by `moviepy`)

### 🔧 Install FFmpeg

- **Windows**:  
  Download from [ffmpeg.org](https://ffmpeg.org), extract it, and add the `bin/` path to your system’s environment variables.

- **macOS**:
  ```bash
  brew install ffmpeg
````

* **Linux (Ubuntu/Debian)**:

  ```bash
  sudo apt update && sudo apt install ffmpeg
  ```

---

### 🔧 Installation Steps

1. **Clone or open your project folder**:

   ```bash
   git clone <your-repo-url>
   cd stuvio_project
   ```

   Or:

   ```bash
   cd C:\Users\divya\Downloads\Documents\project
   ```

2. **Create and activate a virtual environment** (recommended):

   ```bash
   python -m venv venv
   ```

   * **PowerShell**:

     ```bash
     .\venv\Scripts\Activate.ps1
     ```
   * **CMD**:

     ```bash
     venv\Scripts\activate.bat
     ```
   * **macOS/Linux**:

     ```bash
     source venv/bin/activate
     ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**

   Create a `.env` file in the root directory and add:

   ```
   GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY"
   FLASK_SECRET_KEY="YOUR_FLASK_SECRET_KEY"
   ```

---

## 🚀 Run the App

Start the Flask server:

```bash
python api/index.py
```

Open your browser and visit: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🧪 Usage Guide

1. Enter a **topic** on the homepage.
2. Click **Generate Video** or **Generate Quiz**.
3. Wait for the system to process your request.
4. The resulting video or quiz will be displayed on a new screen.

---

## ⚠️ Important Notes

* **Video generation** time may vary depending on the length of the input.
* Make sure **FFmpeg** is properly installed and accessible from your system’s PATH.
* If something goes wrong, **check terminal logs** where Flask is running.
* Be cautious with your **Gemini API usage** — stay within rate limits and check for potential billing.

---

