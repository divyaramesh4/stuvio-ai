# Stuvio AI: Interactive Educational Video & Quiz Generator

## Project Overview

Stuvio AI is a web application designed to enhance learning by generating short, informative videos and interactive quizzes on any given topic. Leveraging AI, it creates engaging content, synthesizes speech, and provides a structured learning experience.

## Features

* **Topic-Based Content Generation:** Input a topic, and the AI generates relevant educational content.
* **Video Creation:** Synthesizes speech from the generated content and combines it with a background image to create short, educational videos.
* **Interactive Quizzes:** Generates multiple-choice quizzes based on the content to test user understanding.
* **Dynamic UI:** Provides a user-friendly interface for seamless interaction.

## Technologies Used

* **Backend:** Flask (Python Web Framework)
* **AI Integration:** Google Gemini API
* **Text-to-Speech:** `gTTS` (Google Text-to-Speech)
* **Video Processing:** `moviepy` (Python library for video editing)
* **Frontend:** HTML, CSS, JavaScript
* **Environment Management (Recommended):** Python `venv`
* **Dependency Management:** `pip`

## Project Structure
Okay, creating a good README.md file is essential for any project! It helps others (and your future self) understand what the project is about, how to set it up, and how to use it.

Here's a comprehensive README.md content suggestion for your "Stuvio AI" educational app. You can copy and paste this into a file named README.md in your project's root directory (C:\Users\divya\Downloads\Documents\project).

Remember to replace placeholder values like YOUR_GEMINI_API_KEY and YOUR_FLASK_SECRET_KEY with your actual information.

Markdown

# Stuvio AI: Interactive Educational Video & Quiz Generator

## Project Overview

Stuvio AI is a web application designed to enhance learning by generating short, informative videos and interactive quizzes on any given topic. Leveraging AI, it creates engaging content, synthesizes speech, and provides a structured learning experience.

## Features

* **Topic-Based Content Generation:** Input a topic, and the AI generates relevant educational content.
* **Video Creation:** Synthesizes speech from the generated content and combines it with a background image to create short, educational videos.
* **Interactive Quizzes:** Generates multiple-choice quizzes based on the content to test user understanding.
* **Dynamic UI:** Provides a user-friendly interface for seamless interaction.

## Technologies Used

* **Backend:** Flask (Python Web Framework)
* **AI Integration:** Google Gemini API
* **Text-to-Speech:** `gTTS` (Google Text-to-Speech)
* **Video Processing:** `moviepy` (Python library for video editing)
* **Frontend:** HTML, CSS, JavaScript
* **Environment Management (Recommended):** Python `venv`
* **Dependency Management:** `pip`

## Project Structure

stuvio_project/

├── ai_video.py  #  Python script for AI/video generation logic
├── index.py
├── static/                # Static assets (CSS, JS, images, generated video output)
│   ├── style.css
│   ├── script.js
│   ├── background.jpg
│   └── (generated videos like output.mp4 will appear here)
├── templates/             # HTML templates for Flask
│   ├── index.html         # Main landing page
│   ├── video_page.html    # Page to display generated video
│   └── quiz_page.html     # Page to display the quiz
├── .env                   # Environment variables (e.g., API keys - NOT committed to Git)
├── requirements.txt       # Python dependencies
└── README.md              # This file
## Setup and Local Installation

Follow these steps to get Stuvio AI running on your local machine.

### Prerequisites

* Python 3.8+ installed.
* `pip` (Python package installer).
* **FFmpeg:** `moviepy` requires FFmpeg to be installed on your system and accessible via your system's PATH.
    * **Windows:** Download a build from [ffmpeg.org/download.html](https://ffmpeg.org/download.html) (e.g., from gyan.dev or BtbN), extract it, and add the path to its `bin` folder (e.g., `C:\ffmpeg\bin`) to your system's Environment Variables `Path`.
    * **macOS:** `brew install ffmpeg`
    * **Linux (Ubuntu/Debian):** `sudo apt update && sudo apt install ffmpeg`

### Installation Steps

1.  **Clone the Repository (if applicable) or Navigate to Project:**
    If you've cloned this project from GitHub:
    ```bash
    git clone <your-repo-url>
    cd stuvio_project
    ```
    Otherwise, navigate directly to your project folder:
    ```bash
    cd C:\Users\divya\Downloads\Documents\project
    ```

2.  **Create and Activate a Virtual Environment (Highly Recommended):**
    While you mentioned not using `venv`, it's best practice for dependency management. If you decide to use it:
    ```bash
    python -m venv venv
    # On Windows (PowerShell):
    .\venv\Scripts\Activate.ps1
    # On Windows (Command Prompt):
    venv\Scripts\activate.bat
    # On macOS/Linux:
    source venv/bin/activate
    ```
    If you choose **not** to use `venv`, skip this step and be aware that dependencies will be installed globally.

3.  **Install Python Dependencies:**
    You will need a `requirements.txt` file listing all your Python dependencies. If you don't have one, or to generate one:
    * Create a file named `requirements.txt` in your project's root directory.
    * Add the following (and any other libraries your `add.py` or `ai_video.py` might use):
        ```
        Flask
        google-generativeai
        moviepy
        gTTS
        python-dotenv # Required if you use .env files
        ```
    * Then install them:
        ```bash
        pip install -r requirements.txt
        ```

4.  **Set Up Environment Variables:**
    Your application requires API keys. Create a file named `.env` in your project's root directory. **Do NOT commit this file to Git.**

    ```
    GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY_HERE"
    FLASK_SECRET_KEY="A_LONG_RANDOM_STRING_FOR_SECURITY"
    ```
    *Replace the placeholder values with your actual keys.*

5.  **Run the Flask Application:**
    Ensure your virtual environment is active (if using one).

    ```bash
    python api/index.py
    ```
    You should see output indicating the server is running.

## Usage

1.  Open your web browser and navigate to `http://127.0.0.1:5000/`.
2.  On the main page, enter a topic for which you want to generate content.
3.  Click the "Generate Video" or "Generate Quiz" buttons.
4.  Wait for the content to be generated. Video generation might take some time depending on the topic length and your system's performance.

## Important Notes

* **Video Generation Performance:** `moviepy` can be CPU-intensive and slow, especially for longer videos. It also requires FFmpeg.
* **API Usage:** Be mindful of API rate limits and costs associated with the Google Gemini API.
* **Error Handling:** The current error message "An error occurred during video/quiz generation. Please try again or check server logs" indicates a backend issue. Always check the terminal where your Flask app is running for detailed Python tracebacks to diagnose problems.

