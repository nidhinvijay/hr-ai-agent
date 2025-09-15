# HR AI Agent 🤖

An intelligent, full-stack web application designed to automate and streamline the initial stages of the recruitment process. This tool allows HR professionals to upload a batch of resumes, provide a job description, and instantly receive an AI-powered analysis and ranking of candidates, complete with automated interview scheduling.

---

## ✨ Key Features

* **AI-Powered Resume Analysis:** Leverages the Google Gemini API to parse and understand resumes, extracting key information like:
    * Overall suitability score (1-100)
    * Detailed summary of qualifications
    * Relevant skills, contact information, and years of experience
* **Dynamic Ranking:** Automatically ranks candidates based on their resume's relevance to the provided job description.
* **Multi-Format File Upload:** Supports the most common resume formats: **.pdf**, **.docx**, and **.txt**.
* **Automated Interview Scheduling:** Integrates with the Google Calendar API to automatically find and schedule interview slots for selected candidates.
* **View Upcoming Interviews:** A built-in feature to fetch and display all scheduled interviews directly from Google Calendar.
* **Modern & Robust UI:** A clean, single-page application with loading spinners, toast notifications for feedback, and client-side validation for a smooth user experience.

---

## 🛠️ Technology Stack

| Category      | Technologies & Tools                                                                        |
| :------------ | :------------------------------------------------------------------------------------------ |
| **Frontend** | HTML5, CSS3, JavaScript (ES6+), Toastify.js                                                 |
| **Backend** | Python, Django, Django REST Framework                                                       |
| **AI & APIs** | Google Gemini API, Google Calendar API                                                      |
| **Python Libs** | `google-generativeai`, `google-api-python-client`, `PyPDF2`, `python-docx`                  |
| **Database** | SQLite (Default for Development)                                                            |

---

## 📸 Screenshots


*The main dashboard for uploading resumes and job descriptions.*


*Ranked candidates with scores, summaries, and extracted skills.*


*The list of upcoming interviews fetched from Google Calendar.*

---

## ⚠️ Important Note for Testers: Google Calendar Access

For security purposes, this application is currently in Google's "Testing" mode. This means only pre-authorized email addresses can grant it access to a Google Calendar during the OAuth consent process.

**I have already pre-authorized the two email addresses from the submission details:**
* `ilmoraai25@gmail.com`
* `devika.rs@srishtiinnovative.com`

If you are logged into a Google account with one of these emails when you test the application, the calendar integration should work seamlessly.

If you would prefer to test using a different Google account, please let me know the email address **(never your password)**, and I will add it to the authorized list immediately. This is a standard procedure for testing new applications that use Google's secure OAuth2 system.

---

## ⚙️ Setup and Installation

Follow these steps to get the project running on your local machine.

### 1. Prerequisites
* Python 3.10+
* `pip` and `venv`

### 2. Clone the Repository
```bash
git clone [https://github.com/your-username/hr-ai-agent.git](https://github.com/your-username/hr-ai-agent.git)
cd hr-ai-agent
```

### 3. Set Up a Virtual Environment
```bash
# Create the virtual environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 4. Install Dependencies
Make sure you have a `requirements.txt` file (generate one with `pip freeze > requirements.txt`).
```bash
pip install -r requirements.txt
```

---

## 🔑 Configuration

This project requires API keys for Google AI and Google Calendar.

### 1. Gemini API Key
* Create a file named `.env` in the root project directory.
* Get your API key from [Google AI Studio](https://aistudio.google.com/).
* Add your key to the `.env` file:
    ```
    GOOGLE_API_KEY=your_gemini_api_key_here
    ```

### 2. Google Calendar API Credentials
* Go to the [Google Cloud Console](https://console.cloud.google.com/).
* Create a new project and enable the **Google Calendar API**.
* Create an **OAuth 2.0 Client ID** for a **Desktop app**.
* Download the JSON file.
* **Rename the file to `credentials.json`** and place it in the root project directory.

---

## ▶️ How to Run

1.  Make sure your virtual environment is activated and all configurations are set.
2.  Run the Django development server:
    ```bash
    python manage.py runserver
    ```
3.  Open your web browser and navigate to:
    ```
    [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
    ```

---
