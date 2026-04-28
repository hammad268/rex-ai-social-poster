🦖 Rex Agent — AI-Powered Social Media Automation
Rex Agent is an end-to-end AI automation system that generates and publishes platform-optimized social media content across Instagram, Facebook, and Threads — all from a single topic input.
🧠 How It Works
You send a topic via a webhook, and Rex Agent handles everything from there:

Content Generation — An AI model (Ollama) generates tailored captions for each platform (Instagram, Facebook, Threads) with proper hashtags and tone.
Image Generation — A separate AI prompt is crafted and sent to the Pollinations AI (Flux model) to generate a matching 1080×1080 image.
Human-in-the-Loop Approval — Before publishing, a confirmation email is sent. You can approve or regenerate the content.
Multi-Platform Publishing — Upon approval, the post is published simultaneously to all three platforms using their respective Graph APIs.
Status Tracking — Each platform's publish result (success/failure) is tracked, merged, and returned as a structured JSON response.

💬 Rex Chat Agent
In addition to the automation pipeline, Rex includes a conversational AI chat agent (powered by Ollama + Simple Memory) for interactive use directly via webhook — useful for Q&A, creative brainstorming, or manual content requests.
🖥️ Frontend (Project_Frontend.html)
A sleek, cinematic single-page web interface for Rex Agent featuring:

A full-screen 3D Spline background with smooth animated transitions
Keyboard-navigable panels (← →) showcasing Rex's capabilities
A built-in Rex popup chat UI with mode selection (Chat / Post Generation)
Dark aesthetic with custom typography, glowing accents, and animated elements

🛠️ Tech Stack
LayerToolsAutomationn8nAI ModelsOllama (local LLM)Image GenPollinations AI (Flux)PlatformsInstagram Graph API, Facebook Graph API, Threads APIFrontendVanilla HTML/CSS/JS + Spline 3DNotificationEmail (SMTP via n8n)
📁 Repository Contents
FileDescriptionRex_Agent_Github.jsonn8n workflow — import directly into your n8n instanceProject_Frontend.htmlRex Agent web UI — open in browserReport.pdfFull project report (LaTeX) with system design & architecture
⚙️ Setup

Import Rex_Agent_Github.json into your n8n instance.
Replace the placeholder tokens (#INSTAGRAM TOKEN, #FACEBOOK TOKEN, THREADS TOKEN) with your actual API credentials.
Make sure Ollama is running locally with your preferred model.
Open Project_Frontend.html in a browser and point it to your n8n webhook URL.
