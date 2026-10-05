AI powered resume ATS scorer using Gemini
🤖 AI Resume Analyzer

An AI-powered Resume Analyzer and ATS Score Generator built using Python, Google Gemini API, and PyPDF2. The system reads a resume in PDF format, extracts the resume content, analyzes it using Gemini, and generates structured insights to help improve the resume.

📌 Project Overview

Recruiters often use Applicant Tracking Systems (ATS) to screen resumes before they are reviewed manually. A resume with missing skills, weak descriptions, or poorly written bullet points may receive a lower ATS score.

This project uses Google Gemini to analyze a candidate's resume and provide useful feedback, including an ATS score, strengths, weaknesses, missing skills, improvement suggestions, and bullet-point rewriting.

🎯 Objectives

- Analyze resumes automatically using Generative AI.
- Extract text from PDF resumes.
- Generate an ATS score out of 100.
- Identify important skills present in the resume.
- Find missing or recommended skills.
- Identify strengths and areas for improvement.
- Provide practical resume improvement suggestions.
- Rewrite resume bullet points to make them more effective.

✨ Features

1. 📊 ATS Score

Generates an overall ATS score out of 100 based on the content and quality of the resume.

2. 💪 Strengths & Weaknesses Analysis

Identifies the strong areas of the resume and points out areas that need improvement.

3. 🔍 Missing Skills Identification

Analyzes the resume and identifies skills that may be missing or could improve the candidate's profile.

4. 📝 Resume Improvement Suggestions

Provides AI-generated recommendations to make the resume clearer, stronger, and more effective.

5. ✍️ Bullet Point Rewriting

Helps rewrite resume bullet points in a more professional and impactful way.

🛠️ Tech Stack

- Python – Core programming language
- Google Gemini API – AI-powered resume analysis
- PyPDF2 – Extracts text from PDF resumes
- Google Colab – Development and execution environment

🔄 System Workflow

Resume PDF
    ↓
Upload Resume
    ↓
Extract Text using PyPDF2
    ↓
Create Structured Prompt
    ↓
Send Resume Text to Google Gemini
    ↓
Gemini Analyzes Resume
    ↓
Generate Structured Insights
    ↓
Display Resume Analysis

⚙️ How It Works

Step 1: Upload Resume

The user uploads a resume in PDF format.

Step 2: Extract Resume Text

The project uses PyPDF2 to read the uploaded PDF and extract its text.

import PyPDF2

def read_resume(file_path):
    text = ""

    with open(file_path, "rb") as file:
        reader = PyPDF2.PdfReader(file)

        for page in reader.pages:
            text += page.extract_text()

    return text

Step 3: Configure Gemini

The extracted resume text is sent to the Google Gemini API using a structured prompt.

The Gemini API is configured using an API key stored securely through Google Colab user data.

Step 4: AI Resume Analysis

Gemini processes the extracted resume and generates structured insights such as:

- Profile Summary
- Key Skills
- Strengths
- Areas of Improvement
- Experience Summary
- Recommended Roles
- Overall ATS Score
- Resume Improvement Tips

Step 5: Generate Results

The generated analysis can be used to understand the resume's strengths and identify areas that can be improved before applying for jobs.

📦 Installation

Install the required Python libraries:

pip install google-genai PyPDF2

🔑 Gemini API Key Setup

You need a Google Gemini API key to run the AI analysis.

In Google Colab, store the API key securely using Colab User Data / Secrets instead of directly writing the key in the notebook.

Example:

from google import genai

client = genai.Client(
    api_key=userdata.get("GOOGLE_API_KEY")
)

«⚠️ Never upload your API key directly to GitHub or hard-code it inside your source code.»

🚀 How to Run the Project

1. Open "AI_resume_analyzer.ipynb" in Google Colab.
2. Install the required dependencies.
3. Configure your Gemini API key securely.
4. Run the notebook cells.
5. Upload your resume in PDF format.
6. The system extracts the resume text using PyPDF2.
7. Gemini analyzes the extracted content.
8. Review the generated ATS score and resume improvement insights.

📂 Project Structure

AI-Resume-Analyzer/
│
├── AI_resume_analyzer.ipynb
│
└── README.md

📊 Analysis Output

The AI Resume Analyzer provides structured feedback including:

Analysis| Description
ATS Score| Overall resume score out of 100
Profile Summary| Short summary of the candidate's profile
Key Skills| Important skills identified from the resume
Strengths| Strong aspects of the resume
Areas of Improvement| Sections that need improvement
Experience Summary| Summary of professional/academic experience
Recommended Roles| Suitable job roles based on the profile
Missing Skills| Skills that could be added or improved
Improvement Tips| Suggestions for improving the resume
Bullet Point Rewriting| More effective versions of resume bullet points

💡 Use Case

This project can be useful for:

- Students preparing resumes for placements
- Freshers applying for jobs and internships
- Job seekers checking their resume quality
- Candidates looking to improve ATS compatibility
- Understanding missing skills and resume improvement areas

🔮 Future Enhancements

- Add Job Description vs Resume matching
- Generate a personalized resume based on a job description
- Add keyword matching and keyword recommendations
- Build an interactive Streamlit web application
- Add downloadable analysis reports
- Add resume comparison for multiple versions
- Add skill-gap analysis based on specific job roles

🎓 Project Highlights

This project demonstrates practical experience with:

- Python programming
- Generative AI
- Google Gemini API
- Prompt engineering
- PDF text extraction
- Structured AI output
- Resume and ATS analysis
- Google Colab

👨‍💻 Author

Nagamani Yegitila

---

⭐ If you find this project useful, consider giving the repository a star!

