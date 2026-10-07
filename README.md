# CrewAI Video Compliance POC

### Proof of Concept for the Azure Multi-Modal Video Compliance & Violation Detection System

This project is a **Proof of Concept (POC)** created to test the core compliance-analysis idea of the main project using **CrewAI, Ollama, Llama 3.2, and Guardrails AI**.

The POC keeps the workflow simple so the multi-agent compliance concept can be tested before integrating it into the larger Azure-based system.

## Main Project

**Azure Multi-Modal Video Compliance & Violation Detection System**

The main project is designed to analyze advertisement videos and identify potential compliance violations using multi-modal AI processing.

This CrewAI project is a simplified POC of that concept.

## POC Flow

```text
Video Transcript + OCR
        ↓
CrewAI Compliance Analyst
        ↓
Compliance Analysis
        ↓
Senior Compliance Reviewer
        ↓
Ollama + Llama 3.2
        ↓
Guardrails AI Validation
        ↓
Final Compliance Report
```

## What This POC Demonstrates

- Multi-agent compliance analysis using **CrewAI**
- Local LLM execution using **Ollama**
- Advertisement compliance analysis
- Detection of potentially misleading or non-compliant claims
- Senior-level review of compliance findings
- Structured output validation using **Guardrails AI**
- Generation of a final compliance report

## Agents

### 1. Compliance Analyst

Analyzes the advertisement transcript/OCR content and identifies possible compliance issues such as:

- Unsupported claims
- Guaranteed results
- Misleading claims
- Health or performance claims

### 2. Senior Compliance Reviewer

Reviews the analyst's findings against the provided compliance rules and produces the final compliance decision.

## Technologies

- Python 3.12
- CrewAI
- Ollama
- Llama 3.2
- Guardrails AI
- Pydantic
- Jupyter Notebook
- `uv`

## Setup

### 1. Create Virtual Environment

```powershell
uv venv --python 3.12
.venv\Scripts\activate
```

### 2. Install Dependencies

```powershell
uv pip install -r requirements.txt
```

### 3. Install and Run Ollama

Install Ollama and make sure it is running.

Pull the model used by the POC:

```powershell
ollama pull llama3.2
```

The POC uses the local Ollama server:

```text
http://localhost:11434
```

### 4. Run the Notebook

Open the notebook in VS Code:

```text
CrewAI_Video_Compliance_Groq_Guardrails_POC_fixed(2).ipynb
```

Run the cells from top to bottom.

## Guardrails Validation

Guardrails AI validates the final LLM response and ensures that the compliance result follows a structured format.

Example:

```json
{
  "status": "PASS",
  "compliance_results": [],
  "final_report": "Advertisement is compliant."
}
```

Possible statuses:

- `PASS`
- `FAIL`
- `REQUIRES_REVIEW`

## Relationship to the Main Project

This is **not the final production system**.

It is a POC created to validate the AI-agent approach for advertisement compliance analysis.

```text
CrewAI Compliance POC
        ↓
Test Agent Workflow
        ↓
Test Compliance Reasoning
        ↓
Test Guardrails Validation
        ↓
Apply Concepts to Main Project
        ↓
Azure Multi-Modal Video Compliance
& Violation Detection System
```

The main project extends this concept with a larger multi-modal architecture for video processing, transcript/OCR extraction, retrieval, Azure services, and production-oriented orchestration.

## Project Structure

```text
.
├── CrewAI Video Compliance POC.ipynb
├── requirements.txt
├── README.md
└── .env
```

## Future Improvements

- Connect real video input
- Automatically extract transcript and OCR
- Add more compliance rules
- Add additional compliance agents
- Add severity and confidence scoring
- Connect the POC with the main Azure compliance system

## Author

**Fardin Khan**

Data Science / AI Engineer
#
