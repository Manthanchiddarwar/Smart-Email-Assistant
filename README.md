# Email Writer Assistant 📧🤖

An AI-powered email reply generator that helps you craft professional responses directly within Gmail. This project consists of a **Spring Boot** backend using the Gemini AI API, a **React (Vite)** frontend for testing/settings, and a **Chrome Extension** for direct Gmail integration.

---

## 🏗️ Project Structure

- **`Email-writer project spring/`**: The backend service built with Spring Boot. It interacts with the Gemini AI to generate email content.
- **`email-writer-react/`**: A modern web dashboard built with React and Vite for managing your email writing preferences.
- **`email-writer.ext/`**: The Chrome Extension that injects an "AI Reply" button into your Gmail compose window.

---

## 🚀 Getting Started

### 1. Backend (Spring Boot)
The backend handles the AI logic and communication with Gemini.

- **Prerequisites**: Java 21, Maven.
- **Setup**:
  1. Navigate to `Email-writer project spring/email-writer-sb`.
  2. Configure your Gemini API Key (usually in `application.properties`).
  3. Run the application:
     ```bash
     mvn spring-boot:run
     ```
- **API Endpoint**: `POST http://localhost:8080/api/email/generate`
  - Body: `{ "emailContent": "...", "tone": "professional" }`

### 2. Frontend (React + Vite)
The frontend provides a user interface for testing and configuration.

- **Prerequisites**: Node.js (v18+ recommended).
- **Setup**:
  1. Navigate to `email-writer-react`.
  2. Install dependencies:
     ```bash
     npm install
     ```
  3. Start the development server:
     ```bash
     npm run dev
     ```

### 3. Chrome Extension
Injects functionality directly into your browser.

- **Setup**:
  1. Open Chrome and navigate to `chrome://extensions/`.
  2. Enable **Developer mode** (top right toggle).
  3. Click **Load unpacked**.
  4. Select the `email-writer.ext` folder from this project.
- **Usage**: Open Gmail, click "Compose" or "Reply", and you'll see a new "AI Reply" button in the toolbar.

---

## ✨ Features

- **AI Reply Generation**: Automatically generates context-aware replies using Google's Gemini AI.
- **Tone Selection**: Choose between professional, casual, or custom tones.
- **Gmail Integration**: Seamlessly integrated into the Gmail UI via a Chrome content script.
- **Real-time Interaction**: Direct insertion of generated text into the compose box.

---

## 🛠️ Tech Stack

- **Backend**: Spring Boot 3.4.2 [check version in pom], Java 21, Spring WebFlux (WebClient).
- **Frontend**: React 19, Vite, Material UI (MUI), Axios.
- **Extension**: Manifest V3, JavaScript, MutationObserver API.

---
