# Snake Game Application  
Self Project — December 2024

A modern web-based implementation of the classic Snake game built using a React.js frontend and a Flask backend. The application supports user authentication, score saving, and persistent high-score tracking using PostgreSQL. Authentication is handled through secure JWT tokens stored in the browser's localStorage, designed to comply with CORS policies.

---

## Features

- Classic Snake game created using React.js.
- User login and signup system with JWT-based authentication.
- High score tracking with scores saved in a persistent database.
- Backend developed with Python Flask and SQLAlchemy ORM.
- PostgreSQL database used for storing user details and score records.
- Secure token storage in localStorage and CORS-compliant API communication.

---

## Tech Stack

### Frontend
- React.js
- Custom game logic built using React components and hooks
- LocalStorage for handling JWT tokens

### Backend
- Python Flask
- SQLAlchemy ORM
- JWT authentication flow
- CORS-compliant REST API

### Database
- PostgreSQL for storing user accounts and score entries


## How It Works

### Authentication Workflow
1. The user signs up or logs in through the React frontend.
2. Upon successful authentication, the Flask backend issues a JWT token.
3. The JWT token is stored in the browser's localStorage.
4. All subsequent API requests include the token for verification.
5. The backend validates the token before granting access to score saving or retrieval.

### Game and Score Flow
- Users play the Snake game directly in the React interface.
- At the end of each game, the score is sent to the Flask backend.
- The backend validates the request, stores the score, and updates high-score records.

---

## Running the Project

### 1. Backend Setup (Flask)
```bash
cd backend
pip install -r requirements.txt
python app.py
