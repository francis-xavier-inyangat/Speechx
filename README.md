# Live Classroom Translation System

## Overview

A comprehensive system that provides real-time language translation for live classroom lectures. The system integrates Fetch.ai agents, a frontend interface, a backend API, and cloud services to ensure seamless and accurate translations. It personalizes learning experiences, adapts to different environments, and provides post-lecture summaries tailored to user preferences.

## Core Features

### 1. Real-Time Translation
- Transcribes and translates live lectures into the user's preferred language and formats like speech to speech, speech to text, and text to speech.

### 2. User Agents
- Personalizes the experience based on learning history and preferences

### 3. Contextual Refinement
- Ensures translations are contextually accurate, especially for academic jargon

### 4. Live Adaptation
- Automatically reroutes requests to alternative services during latency or failures

### 5. Post-Lecture Summary
- Generates a personalized summary of the lecture based on the translated content

## Tech Stack

### Frontend
- **Framework:** React.js
- **Real-Time Updates:** WebSocket
- **Styling:** Material UI

### Backend
- **Language:** Python
- **Framework:** Flask
- **Real-Time Communication:** WebSocket
- **Authentication:** OAuth 2.0 with Google

### Fetch.ai Agents
- **Framework:** Fetch.ai uAgents
- **Agents:**
 	1.	Student Agent:    
	Represents individual users (e.g., students).
	•	Manages user preferences, such as their preferred language for translation.
	•	Handles user requests for real-time transcription and translation, initiating the workflow.

	2.	Broker Agent:
	Acts as an intermediary between the Student Agent and service providers (e.g., transcription and translation services).
	•	Negotiates with available Service Agents to find the best option based on factors like cost, speed, and accuracy.
	•	Ensures fallback mechanisms if a service becomes unavailable or experiences latency.
	3.	Context Agent:
	Focuses on refining translations for domain-specific accuracy.
	•	Ensures that academic jargon, technical terms, or specialized language are translated accurately and appropriately.
	•	Works alongside translation services to improve contextual relevance and precision.

### Cloud Services
- **Transcription:** AWS Transcribe
- **Translation:** Google Cloud Translate API
- **Data Storage:** SQLite
- **Hosting:** GCP