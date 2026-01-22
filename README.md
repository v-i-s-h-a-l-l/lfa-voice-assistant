# LogicVoice AI
# Voice-to-Logic Framework Generator for Social Programs
LogicVoice AI is a system that converts natural conversations into structured Logical Framework Approach (LFA) tables. It is designed to bridge the gap between field-level discussions and the documentation required for professional grant proposals.

# Technical Implementation
This project utilizes a high-performance FastAPI backend and a React frontend connected via WebSockets to provide real-time processing:

WebSockets for Audio: Enables bidirectional data flow, allowing the server to process audio chunks immediately as they are recorded.

Local Whisper Processing: Uses the local Python openai-whisper library for transcription, ensuring data remains on the local machine and eliminating the need for paid external APIs.

Logic Auditor: An AI-driven validation layer that identifies gaps in program logic and prompts the user for missing details during the recording process.

Local-to-Cloud Bridge: Connection maintained via Localtunnel to showcase the local Python server as a live API for the demo.

# Logical Framework (LFA) Structure
The system categorizes program logic into these core components:

Goal: Long-term objective and overall improvement expected.

Outcomes: Specific, measurable changes for beneficiaries.

Indicators: Quantitative or qualitative measures used to track outcomes.

Outputs: Concrete deliverables and direct results of program activities.

Activities: Ground-level tasks performed.

Responsibility & Monitoring: Accountability and implementation tracking.

# How to Run Locally
1. Backend Setup (FastAPI)
Ensure you have Python 3.12+ and FFmpeg installed on your system.

Bash
# Navigate to project root
cd logicvoice-ai
# Navigate to the backend directory
cd backend

# Install required dependencies
pip install fastapi uvicorn openai-whisper python-multipart

# Run the FastAPI server
uvicorn api.main:app --reload

# Navigate to frontend folder
cd frontend

# Install Node modules
npm install

# Start the development server
npm run dev
