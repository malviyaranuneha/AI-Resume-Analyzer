
# AI Resume Analyzer

An AI-powered resume analysis and job-matching automation built with **n8n, Groq AI, Gmail, and Google Sheets**.

## Project Overview

The AI Resume Analyzer compares a candidate's PDF resume against a job description and target role. It generates a structured, AI-powered analysis report, emails the results to the candidate, and records submission details in Google Sheets.

The project demonstrates workflow automation, generative AI integration, document processing, and Google Workspace integration.

## Key Features

- PDF resume upload through an n8n form
- AI-based comparison of resume and job description
- Estimated ATS match score (not an official ATS score)
- Matching and missing skill analysis
- Resume strengths and improvement suggestions
- Role-specific interview preparation tips
- Formatted HTML analysis report delivered by Gmail
- Submission and analysis records stored in Google Sheets

## Technology Stack

| Technology | Purpose |
| --- | --- |
| n8n | Workflow automation and form handling |
| Groq AI | Large language model inference |
| GPT-OSS 20B | Resume analysis and report generation |
| JavaScript / Node.js | Local form proxy for temporary testing |
| Cloudflare Quick Tunnel | Temporary HTTPS access for testing |
| Gmail API | Automated email delivery |
| Google Sheets API | Submission and report logging |

## How It Works

1. A candidate uploads a PDF resume and provides a job description, target role, and email address.
2. n8n extracts text from the uploaded PDF.
3. Groq AI compares the extracted resume text with the job requirements.
4. The AI produces a six-section analysis report.
5. n8n converts the Markdown report to HTML.
6. Gmail sends the formatted report to the submitted email address.
7. Google Sheets records the submission information and AI-generated analysis.

## Report Sections

1. Estimated ATS Match Score
2. Matching Skills
3. Missing Skills
4. Resume Strengths
5. Resume Improvement Suggestions
6. Interview Preparation Tips

**Note:** The ATS match score is an AI-generated estimate and is not produced by a commercial applicant tracking system.

## Workflow File

[View the sanitized n8n workflow](./AI_Resume_Analyzer_GitHub_Sanitized.json)

The workflow file is provided without configured credentials or a personal spreadsheet destination.

## Setup Instructions

1. Install and start n8n.
2. Import the sanitized workflow JSON into n8n.
3. Configure a Groq API credential and select the supported model.
4. Configure Gmail and Google Sheets OAuth credentials.
5. Select your own Google spreadsheet and map the required columns.
6. Publish the workflow and test it with a sample PDF resume.
7. Review the workflow settings and data-handling practices before allowing public submissions.

## Live Demo

A temporary local-hosted demonstration has been tested using Cloudflare Quick Tunnel. A permanent public demo is not currently available.

## Privacy and Limitations

- Do not submit sensitive personal information to an untrusted demo.
- Submitted resume information is processed by an external AI service.
- Submission details and generated reports may be stored in Google Sheets and n8n execution history.
- AI-generated feedback and match scores can be inaccurate and should be reviewed critically.
- Public deployments should include access controls, abuse prevention, retention policies, and appropriate privacy disclosures.

## Project Status

**Working prototype:** Resume upload, PDF extraction, AI analysis, email delivery, and Google Sheets logging have been tested successfully.

**Planned improvements:** Permanent hosting, stronger public-access controls, privacy safeguards, and improved deployment documentation.
  
