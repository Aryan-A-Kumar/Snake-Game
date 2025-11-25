# Snake Game Application  
Self Project — December 2024

A modern web-based implementation of the classic Snake game built using a React.js frontend and a Flask backend. The application includes user authentication, score saving, and persistent high-score tracking using PostgreSQL. Authentication is handled through secure JWT tokens stored in the browser’s localStorage, fully compliant with CORS policies.

---

## Features

- Classic Snake game built using React.js.
- User login and signup system with JWT-based authentication.
- High-score tracking with persistent storage in PostgreSQL.
- Backend implemented in Python Flask with SQLAlchemy ORM.
- Secure token handling through localStorage.
- CORS-compliant communication between frontend and backend.

---

## Tech Stack

### Frontend
- React.js  
- Custom game logic implemented using React components and hooks  
- JWT storage using browser localStorage  

### Backend
- Python Flask  
- SQLAlchemy ORM  
- JWT authentication  
- REST API with CORS enabled  

### Database
- PostgreSQL for persistent storage of users and scores  

---

## How It Works

### Authentication Flow
1. Users sign up or log in through the React frontend.  
2. The Flask backend verifies credentials and issues a JWT token.  
3. The token is saved in the browser's localStorage.  
4. Future API requests automatically include the JWT for verification.  
5. Flask validates the token before allowing secure operations such as saving scores.

### Game and Score Handling
- The Snake game runs fully in the React frontend.  
- After each game, the score is sent to the backend API.  
- The backend verifies the user's token, stores the score, and updates the leaderboard.

---

## Running the Project

### 1. Backend Setup (Flask)
```bash
cd backend
pip install -r requirements.txt
python app.py
```
2. Frontend Setup (React)
```bash
cd frontend
npm install
npm run dev
```
3. Database Setup (PostgreSQL)

Ensure PostgreSQL is running.

Create the database:

CREATE DATABASE snakegame;


Update database connection details in the Flask backend configuration.

Run migrations or allow SQLAlchemy to automatically create tables on first run.
