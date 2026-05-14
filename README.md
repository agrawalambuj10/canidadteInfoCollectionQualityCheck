# Candidate Information Collection QA System

Candidates are manually called to collect important information such as:
- Current Salary
- Expected Salary
- Notice Period
- Preferred Location

This information is then entered into an internal dashboard accessed by client companies.

Due to the manual nature of the process and high operational volume, data mismatches regularly occurred between:
- what the candidate actually communicated on call
- and what was manually entered by the POC

This created a poor client experience and made manual QA checks infeasible at scale.

---

## Solution

Built an AI-powered QA workflow to automatically verify candidate information collected during calls.

The system:
1. Transcribes candidate calls using AI.
2. Extracts structured information from the transcript.
3. Compares extracted values against manually entered dashboard values.
4. Flags mismatches for review.

This significantly reduced manual QA effort, improved data accuracy shared with clients and enabled tracking of POC performance quality.
---

## Workflow

### Step 1 — Call Transcription
`callTranscription`

- Uses OpenAI API to transcribe candidate calls.
- Converts raw audio into structured text transcripts.

### Step 2 — Information Extraction + QA Matching
`matchFilledDeetsWithTranscribed`

- Extracts fields such as:
  - Current Salary
  - Expected Salary
  - Notice Period
  - Location
- Understands conversational context using AI.
- Compares extracted values against manually entered POC data.
- Flags discrepancies for QA review.

---

## Tech Stack

- JavaScript
- OpenAI APIs
- AI Prompting
- Airtable
- Internal API
