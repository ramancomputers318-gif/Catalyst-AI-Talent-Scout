**Catalyst AI: Intelligent Talent Scouting & Engagement Agent**
**Hackathon: Deccan AI Catalyst (April 2026)**

**Developer: Raman Jeet**

**Role Category: AI Agent Developer**

**The Challenge (Problem Statement):**
Recruiters are currently burdened by "Application Fatigue," manually sifting through hundreds of candidate profiles to find specific technical matches.

**The Task**: Create an AI Agent that automates candidate discovery, provides explainable scoring (Match & Interest), and drafts personalized outreach messages.

**The Solution**: Catalyst Scout with Auto-Model Detection
My solution is a resilient AI Agent that features Dynamic Model Discovery. Unlike standard implementations that hard-code a specific model version, my agent is built to be "future-proof."

**Key Features:**
Smart Brain Detection: The agent scans the user's Google Cloud project in real-time to identify which Gemini models are available and automatically selects the highest-performing engine (e.g., Gemini 2.5 Flash).

Semantic Analysis: The agent uses high-level reasoning to understand candidate project impact (like "HireBot") rather than simple keyword matching.

Dual-Metric Scoring: Provides a Match Score (technical fit) and an Interest Score (career alignment).

Automated Outreach: Generates unique, professional messages tailored to each candidate's specific background.

**System Architecture:**
The agent follows a logical flow from environmental setup to final recruitment output.

Model Discovery: The system queries genai.list_models() to detect available Gemini versions in the connected Google account.

Selection Logic: The agent autonomously chooses the best available brain (detected as Gemini 2.5 Flash) to ensure processing reliability.

Data Ingestion: Accepts raw text from JDs and Candidate Profiles.

Reasoning & Scoring: Performs semantic comparison to generate scores and outreach drafts.

Technical Implementation (The "Auto-Brain" Logic)
I implemented a robust setup in Section 1 of the code:

The Discovery Part: **genai.list_models()** — This function acts as a scout, searching through all possible generative models allowed by the API key.

The Decision Part: **available_models[0]** — The agent automatically decides to use the first and most capable brain it finds, ensuring the system never fails due to a hard-coded model name being deprecated.

**Technical Stack:**
Model Detection Engine: Google Generative AI Discovery

Core Model: Gemini 2.5 Flash

Language: Python 3.12

Environment: Google Colab

**How to Run**
Open the .ipynb file in Google Colab.

Add your API Key to the Secrets tab (Key icon) with the name GOOGLE_API_KEY.

Run the code cell. The agent will print:  System Ready: Using model models/gemini-2.5-flash once it detects your account's capabilities.

Paste your JD and Candidate details when prompted.

 **Project Deliverables**
Demo Video: https://drive.google.com/file/d/1fpwDcbBCv60cQnhuTfwFFP8sg327PRc2/view?usp=sharing

Live Notebook: https://colab.research.google.com/drive/1lDNbn3cYmIuGAETqwGRvlQUZ26-RwGLJ?usp=sharing

Architecture-Diagram: https://drive.google.com/file/d/1b2vGHqzxtvfAQiTHf-1AldJ7WheyFcLy/view?usp=sharing

Documentation: README.md
