# AI Resume Analyzer

AI-powered tool that helps job seekers match their resumes against job descriptions.  
Upload your resume (PDF/TXT) and paste a job description to instantly see your Match Score and Missing Keywords.

Built with **FastAPI, scikit-learn, spaCy** (backend) and **React + TypeScript + Material UI** (frontend).

---

## Features

- Upload resume (PDF or TXT)
- Paste full job description
- Instant Match Score (%) with color-coded progress bar
- Highlights missing keywords as badges
- Clean UI with Material UI components
- Full-stack integration (FastAPI + React)

---

## Demo

_(Add screenshots here — UI with file upload + results)_

---

## Tech Stack

**Backend:**

- FastAPI
- scikit-learn (TF-IDF + cosine similarity)
- spaCy (text processing)
- pdfplumber (PDF parsing)

**Frontend:**

- React + TypeScript
- Material UI
- Axios (API calls)
- Vite (bundler)

---

## Getting Started

### Clone the repo

```bash
git clone https://github.com/yourusername/ai-resume-analyzer.git
cd ai-resume-analyzer
```

## Backend Setup

1. Navigate to the backend folder:

   ```bash
   cd backend
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   .\.venv\Scripts\activate   # Windows PowerShell
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Start the FastAPI server:
   ```bash
   uvicorn backend.main:app --reload --port 8000
   ```

**The backend API will be available at:**

- http://127.0.0.1:8000
- Swagger UI for testing: http://127.0.0.1:8000/docs

## Frontend Setup

1. Navigate to the frontend folder:

   ```bash
   cd frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

**Frontend will run at:** http://127.0.0.1:5173

---

## Example Usage

1. Upload your resume.pdf
2. Paste a job description
3. Click Analyze

**Example response:**

```json
{
  "filename": "resume.pdf",
  "score": 72.45,
  "missing_keywords": ["react", "ai", "experience"]
}
```

---

## Why this project?

Applicant Tracking Systems (ATS) often filter candidates by keyword matching.  
This project simulates that process, helping job seekers tailor their resumes for higher chances of being noticed.

---

## License

MIT License – feel free to use and adapt.

---

## API

**POST /analyze**

```json
{
  "resume_file": "file_upload",
  "job_description": "string"
}
```

**Response:**

```json
{
  "match_score": 78.5,
  "missing_keywords": ["Python", "Docker", "AWS"],
  "matched_keywords": ["JavaScript", "React"]
}
```

---

## Docker

```bash
docker-compose up --build
```

---

## License

MIT License
