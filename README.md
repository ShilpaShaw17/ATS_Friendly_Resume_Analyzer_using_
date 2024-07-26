environment:
conda create -p venv python==3.10 -y


env:
.env to store Google API key




Overview

ATS Resume Expert is a Streamlit application designed to evaluate resumes against job descriptions using advanced AI. The app leverages Google's Gemini Pro Vision model to provide insights on how well a resume aligns with job requirements and offers suggestions for improvement.

Features

Resume Evaluation: Assess how well the applicant's resume matches the job description.
Skill Improvement Suggestions: Receive feedback on how to enhance the resume's effectiveness.
Percentage Match: Determine the percentage match between the resume and the job description.
Prerequisites
Python 3.7 or higher
Required Python packages:
streamlit
dotenv
base64
PIL (Pillow)
pdf2image
google-generativeai



Usage

Run the Streamlit app:

streamlit run app.py

Open your browser and go to http://localhost:8501 to interact with the app.

Upload your resume (PDF) and enter the job description in the provided text area.

Choose one of the following actions:

"Tell Me About the Resume": Get a detailed evaluation of how well the resume fits the job description.
"How Can I Improvise my Skills": Receive suggestions on how to improve the resume.
"Percentage Match": Obtain a percentage match between the resume and job description.
Functionality
input_pdf_setup: Converts the uploaded PDF resume into an image format for processing.
get_gemini_response: Communicates with Google's Gemini Pro Vision model to generate responses based on the input and resume content.
