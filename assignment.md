# Meeting Prep Assistant — Assignment Submission

## 📌 Overview

This project implements a **Meeting Prep Assistant** using Google AI Studio and Gemini models. The system processes uploaded meeting notes (PDF) and presentation slides to generate structured meeting intelligence.

The output includes:
- Meeting summary  
- Key risks  
- Talking points  
- Next steps  
- Cover image prompt  

The solution demonstrates prompt engineering, structured outputs, UX generation using Stitch, and optional deployment workflows.

---

## 🏗️ Architecture

### 🔹 Core Components

**Frontend (UX)**
- Designed using Stitch  
- Includes:
  - File upload interface  
  - Results dashboard  
- Exported as PNG screens  

**AI Layer**
- Google AI Studio  
- Gemini models:
  - `gemini-2.5-flash`
  - `gemini-2.5-pro`

**Prompt Layer**
- Structured JSON schema  
- Grounded extraction logic  
- Constraints to avoid hallucination  

**Input Data**
- Meeting Notes (PDF)  
- Presentation Slides  

---

### 🔹 Processing Flow

1. User uploads meeting documents  
2. Prompt is executed via Gemini  
3. Model extracts structured insights  
4. Output returned in JSON format  
5. Results displayed in UI  

---

### 🔹 Output Schema

```json
{
  "summary": "",
  "risks": [
    { "risk": "", "evidence": "" }
  ],
  "talking_points": [
    { "point": "", "why_it_matters": "" }
  ],
  "next_steps": [
    { "action": "", "owner_if_known": "", "due_date_if_known": "" }
  ],
  "cover_image_prompt": ""
}
