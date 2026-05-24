# Meeting Prep Assistant — Assignment Submission

## Overview

This project implements a **Meeting Prep Assistant** using Google AI Studio and Gemini models. The system processes uploaded meeting notes (PDF) and presentation slides to generate structured meeting intelligence.

The output includes:
- Summary of the meeting
- Identification of risks
- Key stakeholder talking points
- Recommended next steps
- A cover image prompt representing the meeting context

The solution demonstrates structured prompt engineering, iterative refinement, and UX generation using Stitch.

---

## Architecture

### Core Components

**1. AI Layer**
- Built using Google AI Studio
- Utilises Gemini models:
  - `gemini-2.5-flash` (fast iteration)
  - `gemini-2.5-pro` (improved reasoning)

**2. Prompt Layer**
- Designed using structured prompts
- Enforces strict output schema
- Includes grounding rules to prevent hallucination

**3. Input Layer**
- Meeting Notes (PDF)
- Presentation Slides

**4. UX Layer**
- Designed using Stitch
- Includes an upload interface and results dashboard

---

### Processing Flow

1. User uploads meeting notes and slides  
2. Prompt is executed in Google AI Studio  
3. Gemini model analyses content  
4. Structured JSON output is generated  
5. Results are displayed in UX screens  

---

## Output Schema

The system enforces a strict JSON format:

```json
{
  "summary": "",
  "risks": [
    {
      "description": "",
      "impact": "High | Medium | Low"
    }
  ],
  "talking_points": [],
  "next_steps": [
    {
      "action": "",
      "owner": ""
    }
  ],
  "cover_image_prompt": ""
}
