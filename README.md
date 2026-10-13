
# ClinIQ AI – Medical Voice Agent

An AI-powered medical consultation application that provides symptom-based specialist recommendations and real-time voice consultations with an AI doctor. The platform allows users to describe their symptoms, choose a recommended specialist, participate in a voice conversation, and receive a consultation report.

## Overview

ClinIQ AI simplifies access to preliminary medical guidance through an interactive, voice-based consultation experience. Users authenticate through Clerk and are redirected to a dashboard where they can enter their symptoms and receive specialist recommendations generated using Gemini AI.

After selecting a specialist, the application saves the selection in the database and generates a unique consultation session ID using `uuidv4`. A dedicated session page is opened where Vapi AI enables a real-time voice conversation between the user and the AI doctor.

After the consultation, Gemini AI generates a report summarizing the discussion, including symptoms, identified concerns, recommendations, and medication-related information.

## Key Features

- **User Authentication:** Uses Clerk for user sign-up and login, stores user information, and redirects authenticated users to the dashboard.
- **Symptom-Based Specialist Recommendations:** Accepts user symptoms through a dialog box and uses Gemini AI with predefined medical agent prompts to suggest relevant specialists.
- **Specialist Selection:** Allows users to select a specialist from the suggested options and saves the selection through a backend function.
- **Unique Consultation Sessions:** Generates a unique session ID using `uuidv4` and opens a dedicated page for each consultation.
- **Real-Time Voice Consultation:** Integrates Vapi AI for speech-to-text and text-to-speech, enabling natural voice conversations with an AI doctor.
- **AI-Powered Consultation Reports:** Generates a report after the conversation containing symptoms, concerns, recommendations, and medication-related information.
- **Database Management:** Uses Drizzle ORM to manage application data, including user information, selected specialists, consultation sessions, and reports.

## Technology Stack

- **Next.js** - Application framework and user interface
- **TypeScript** - Type-safe application development
- **Clerk** - User authentication
- **Vapi AI** - Real-time voice interaction, speech-to-text, and text-to-speech
- **Gemini AI** - Specialist recommendations and consultation report generation
- **Drizzle ORM** - Database access and data management
- **UUID** - Generation of unique consultation session IDs
- **Tailwind CSS** - Application styling

## Architecture Diagram

<img width="1774" height="887" alt="image" src="https://github.com/user-attachments/assets/a7a2ecf0-1661-4f95-9aaa-1eb95374d481" />

## How It Works

### 1. User Authentication

- Users sign up or log in using Clerk.
- User information is stored in the database.
- After successful authentication, users are redirected to the dashboard.

### 2. Symptom Entry and Specialist Recommendation

- The dashboard displays a dialog box where users enter their symptoms.
- The symptoms are sent to a backend function.
- The backend uses Gemini AI along with predefined medical agent prompts to identify suitable specialists.
- The recommended specialists are displayed for the user to choose from.

### 3. Specialist Selection and Session Creation

- The user selects a specialist from the recommendations.
- The selected specialist is saved in the database through a backend function.
- The application generates a unique session ID using `uuidv4`.
- A dedicated consultation page is opened using the session ID.

### 4. Real-Time Voice Consultation

- The consultation page integrates Vapi AI as the voice agent.
- Speech-to-text converts the user's spoken input into text.
- The AI doctor processes the conversation and responds using text-to-speech.
- The user and AI doctor participate in a real-time conversation about the reported symptoms and related concerns.

### 5. Consultation Report Generation

- After the conversation ends, the consultation details are used to generate a report.
- Gemini AI produces a structured summary of the consultation.
- The report includes symptoms, concerns discussed, recommendations, and medication-related information.
- The report is stored in the database and presented to the user.

## Benefits

- Provides an interactive voice-based consultation experience.
- Recommends relevant medical specialists based on user-reported symptoms.
- Uses unique session IDs to organize individual consultations.
- Generates structured reports to summarize conversations.
- Combines conversational AI, voice technology, and database management in a single application.

## Setup

- Install dependencies using the package manager configured in `package.json`.
- Configure the required Clerk, Gemini AI, Vapi AI, and database environment variables.
- Run the development command defined in `package.json`.
- Keep API keys and credentials in environment variables and never commit secrets to Git.

## Disclaimer

ClinIQ AI is an AI-powered medical guidance project and is not a substitute for professional medical diagnosis, treatment, or emergency care. AI-generated recommendations may be inaccurate and should be reviewed by a qualified healthcare professional.
