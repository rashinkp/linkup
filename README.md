💬 LinkUp Chat

A full-stack real-time messaging application with separate backend and frontend services. Handles authentication, message delivery, media uploads, and socket-based live chat.

🚀 Tech Stack
Backend

Node.js, Express

Socket.IO (real-time messaging)

Cloudinary (media)

Database (configured in backend/src/lib/db.js)

Frontend

React + Vite

Local store for state

UI Components & pages

Additional Tooling

ESLint

Vite

React Router

📁 Project Structure
LinkUp Chat/
│
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── lib/
│   │   ├── routes/
│   │   └── server.js
│   └── ...
│
└── frontend/
    ├── src/
    │   ├── pages/
    │   ├── components/
    │   ├── store/
    │   ├── App.jsx
    │   └── main.jsx
    └── ...

🔍 Important Directories & Files
Backend

Server entry → backend/src/server.js

Socket helpers → backend/src/lib/socket.js

exports: io, server, getReceiveSocketId

Cloudinary helper → backend/src/lib/cloudinary.js

DB connection → backend/src/lib/db.js

Controllers:

auth.controller.js

message.controller.js

Models:

user.model.js

message.model.js

Middleware:

auth.middleware.js

Frontend

Entry → frontend/src/main.jsx

App shell → frontend/src/App.jsx

Pages → example: LoginPage.jsx

Store → frontend/src/store/

⚙️ Running the Project
1️⃣ Install Dependencies
cd backend
npm install

cd ../frontend
npm install

2️⃣ Configure Environment Variables
Backend .env
PORT=5000
DB_URL=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
JWT_SECRET=

Frontend .env
VITE_BACKEND_URL=http://localhost:5000

3️⃣ Start Backend
cd backend
npm run dev

4️⃣ Start Frontend
cd frontend
npm run dev

⚡ Realtime Messaging Logic

User connects to server

Socket.IO assigns & stores socketId

Messages are sent via API

Backend emits to receiver socket

UI updates instantly

🧩 Features

Realtime private chat

Login & authentication

Online user system

Message storage

Cloudinary media upload

Clean folder-level separation

🛠️ Key Libraries Used

express

socket.io

cloudinary

react

react-router-dom

lucide-react

🚧 Future Upgrades

Group chat

Message seen/typing indicators

Push notifications

Deployment setup

⭐ Final Notes

This project is structured for clarity and separate responsibility between backend and frontend. Socket logic, controllers, middleware, and models are isolated properly, and the frontend uses Vite with a clean component layout.