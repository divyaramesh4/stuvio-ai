

## 📌 Project Overview

**Stuvio AI** is a web application designed to enhance learning by generating short, informative videos and interactive quizzes on any given topic. Leveraging **AI**, it creates engaging content, synthesizes speech, and provides a structured learning experience.

---

## ✨ Features

- 📚 **Topic-Based Content Generation** – Input a topic and generate relevant educational content.
- 🎥 **Video Creation** – Synthesizes speech and combines it with a background image.
- 📝 **Interactive Quizzes** – Tests understanding with MCQs based on the topic.
- 💻 **Dynamic UI** – Smooth and user-friendly interface.

---

## 🛠️ Technologies Used

- **Backend**: Flask (Python Web Framework)  
- **AI Integration**: Google Gemini API  
- **Text-to-Speech**: gTTS (Google Text-to-Speech)  
- **Video Processing**: moviepy  
- **Frontend**: HTML, CSS, JavaScript  
- **Environment Management**: Python `venv`  
- **Dependency Management**: pip  

---

## 📁 Project Structure

- `ai_video.py` – Python script for AI/video generation logic  
- `index.py` – Main server file  
- `static/` – Static assets  
  - `style.css` – Custom styling  
  - `script.js` – JavaScript for interactivity  
  - `background.jpg` – Background image used in videos  
  - `output.mp4` – Generated video (appears here)  
- `templates/` – HTML templates  
  - `index.html` – Main landing page  
  - `video_page.html` – Displays the generated video  
  - `quiz_page.html` – Displays quiz questions  
- `.env` – Stores environment variables (keep secret)  
- `requirements.txt` – Lists Python dependencies  
- `README.md` – This file  

---

## 🧩 Setup and Local Installation

### ✅ Prerequisites

- Python 3.8+
- pip (Python package installer)
- FFmpeg (required for moviepy)

### 🔧 Install FFmpeg

- **Windows**: Download from [ffmpeg.org](https://ffmpeg.org), extract, and add `bin/` folder to PATH  
- **macOS**:

  brew install ffmpeg


* **Linux (Ubuntu/Debian)**:

  ```bash
  sudo apt update && sudo apt install ffmpeg
  ```

---

### 🔧 Installation Steps

1. **Clone the repository** or move to the project folder:

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

   * Windows PowerShell:

     ```bash
     .\venv\Scripts\Activate.ps1
     ```
   * Windows CMD:

     ```bash
     venv\Scripts\activate.bat
     ```
   * macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

3. **Install required packages**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**

   Create a `.env` file in the root folder with:

   ```
   GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY"
   FLASK_SECRET_KEY="YOUR_FLASK_SECRET_KEY"
   ```

---

## 🚀 Run the App

```bash
python api/index.py
```

Visit [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

---

## 🧪 Usage

1. Enter a topic in the input box.
2. Click **Generate Video** or **Generate Quiz**.
3. Wait for the AI to generate the result.
4. The video/quiz will be displayed on a new page.

---

## ⚠️ Important Notes

* **Video generation** may be slow for long topics.
* **FFmpeg** must be properly installed for moviepy to work.
* **Check terminal logs** for debugging if you see error messages in the browser.
* **Gemini API** usage may be limited or charged—check your usage.

---

