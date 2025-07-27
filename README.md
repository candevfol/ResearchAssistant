# Research Assistant

## About

Research Assistant is a two-part tool combining a Java Spring Boot backend and a Chrome browser extension. The backend exposes a REST API that leverages Google Gemini AI to summarize or suggest topics for user-provided text. The Chrome extension allows users to select text on any webpage, send it to the backend for AI-powered summarization, and take/save research notes locally. Communication between the extension and backend is handled via HTTP POST requests, and the backend is easily configurable via environment variables for Gemini API access.

## Setup

### Backend (Spring Boot)
1. **Requirements:** Java 17+, Maven (or use the provided Maven Wrapper).
2. **Configure Gemini API:**
   - Set the `GEMINI_KEY` environment variable to your Gemini API key.
   - The backend uses `src/main/resources/application.properties` for configuration.
3. **Run the backend:**
   ```sh
   cd research-assistant
   ./mvnw spring-boot:run
   ```
   The backend will start on `http://localhost:8080`.

### Browser Extension
1. Open Chrome and go to `chrome://extensions/`.
2. Enable "Developer mode" (top right).
3. Click "Load unpacked" and select the `research-assistant-ext` directory.

## How to Use

1. **Start the backend** if not already running.
2. **In Chrome, select any text** on a webpage.
3. **Open the Research Assistant extension** (side panel or extension icon).
4. Click **"Summarize"** to send the selected text to the backend and receive an AI-generated summary.
5. Use the **notes area** in the extension to take and save research notes locally.
