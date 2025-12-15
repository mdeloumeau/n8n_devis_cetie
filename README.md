Electrical Cabinet Quote Automation Workflow

This repository contains an n8n workflow that automates the process of extracting and analyzing emails, PDFs, and Excel files to generate structured information for electrical cabinet (or control panel) quote requests.

Features

 - Email Trigger: Automatically triggers when a new email is received in Microsoft Outlook.
 - Attachment Extraction: Extracts PDF and Excel attachments from emails.
 - Text Cleaning: Cleans email body text by removing HTML and unnecessary content.
 - AI Analysis: Uses LangChain models (Mistral Cloud & Codestral) to:
    - Detect if the email concerns an electrical cabinet quote request.
    - Summarize PDF and Excel attachments.
    - Extract technical details, options, regulation devices, and deadlines.
 - JSON Output: Creates a structured JSON containing:
    - Client name
    - Contact person
    - Cabinet details (title, options, regulation)
    - Requested deadline
    - Attachments
    - Notes
 - HTML Report: Generates a clean HTML summary of the quote request.

Workflow Overview

 1- Trigger: Microsoft Outlook email received.
 2- Clean Email: Remove HTML and unnecessary parts of the body.
 3- Detect Quote Request: AI determines if the email is relevant.
 4- Extract Attachments: PDFs and Excel files are extracted and processed.
 5- Summarize Content: AI summarizes technical content related to cabinets.
 6- Build JSON: Structured data is created for quote preparation.
 7- Validation: Ensures extracted data is valid and not empty.
 8- Generate HTML: Creates a readable report for review.

Requirements

 - n8n (latest version)
 - Microsoft Outlook integration
 - LangChain nodes for AI models
 - Access to Mistral Cloud and Codestral AI models

How to Use

 - Import the workflow into your n8n instance.
 - Configure your Microsoft Outlook credentials.
 - Set up Mistral Cloud and Codestral API keys.
 - Activate the workflow.
 - Emails with relevant quote requests will automatically be processed, and a structured HTML summary will be generated.

Notes

Only extracts data explicitly present in the email or attachments — no assumptions are made.

Supports both PDF and Excel attachments.

Designed for electrical cabinet (armoire) quote requests.
