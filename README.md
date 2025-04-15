# SnapNote-project

# SnapNote - A Note-Sharing App

SnapNote is a full-stack note-sharing application where users can create, view, and manage notes with tags. The app is built using React for the frontend, Express for the backend, and MongoDB for the database.

## Features

- Create, view, and delete notes.
- Filter notes by tags.
- Responsive design for mobile and desktop.

## Tech Stack

- **Frontend**: React, React Router, Axios, CSS
- **Backend**: Express.js
- **Database**: MongoDB (Local or Atlas)

## Prerequisites

Before running the project, ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/) (v14 or above)
- [MongoDB](https://www.mongodb.com/try/download/community) (if running locally)
- [Git](https://git-scm.com/)
- [Nodemon](https://www.npmjs.com/package/nodemon) (for automatic server restarts, optional)

## Setup Instructions

### 1. Clone the GitHub Repository

Clone the repository to your local machine using the following command:

```bash
git clone [https://github.com/your-username/SnapNote.git](https://github.com/your-username/SnapNote.git)
2. Install Backend Dependencies
Navigate to the backend directory and install the necessary dependencies:

Bash

cd SnapNote/backend
npm install
3. Setup Environment Variables
Create a .env file inside the backend directory. Add your MongoDB connection string (if using MongoDB Atlas, or set up your local MongoDB URI):

Plaintext

MONGODB_URI=mongodb://localhost:27017/snapnote
PORT=5000
If using MongoDB Atlas, replace the MONGODB_URI with your Atlas connection string.

4. Start the Backend Server
Run the backend server using nodemon or node:

Bash

npm run dev   # To run with nodemon (auto-restarts on changes)
# OR
npm start     # To run with node
The backend should now be running on http://localhost:5000.

5. Install Frontend Dependencies
Navigate to the frontend directory and install the necessary dependencies:

Bash

cd SnapNote/frontend
npm install
6. Start the Frontend Development Server
Start the React development server:

Bash

npm run dev
The frontend should now be running on http://localhost:3000.

7. Open the Application
Visit http://localhost:3000 in your browser to access the frontend of the SnapNote application. The backend will be handling the API requests at http://localhost:5000/api/notes.

8. Optional - Seed Some Initial Notes (Optional)
If you want to quickly populate your database with some notes, you can either manually add them via the frontend or create a simple script to seed data (this is optional).

9. Optional - MongoDB Atlas Setup (For Cloud Database)
If you want to use MongoDB Atlas, follow these steps:

Create a MongoDB Atlas cluster (if you haven't already).
Get your connection string from the Atlas console.
Replace the MONGODB_URI in your .env file with the connection string from MongoDB Atlas.
You may need to whitelist your IP address in MongoDB Atlas to allow connections.
Troubleshooting
Backend server not starting:

Ensure MongoDB is running on your machine (if using local MongoDB).
Check the .env file for the correct MONGODB_URI and PORT.
Frontend not loading:

Ensure that the backend server is running and accessible on http://localhost:5000.
Check the baseURL in your Axios calls to confirm the correct API endpoint.
CORS issue:

If you are getting CORS errors while trying to connect the frontend to the backend, make sure to add the following to your backend code to enable CORS:
JavaScript

import cors from 'cors';
app.use(cors());
Folder Structure
Bash

SnapNote/
├── backend/                # Backend (Express & MongoDB)
│   ├── controllers/        # API controllers
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── .env                # Environment variables (MongoDB URI, PORT)
│   ├── server.js           # Express server setup
│   └── package.json        # Backend dependencies and scripts
│
├── frontend/               # Frontend (React app)
│   ├── src/                # Source code for React app
│   │   ├── components/     # Reusable React components (Home, NoteDetail, CreateNote, etc.)
│   │   ├── services/       # Axios API calls
│   │   ├── App.js          # Main React app component
│   │   └── index.js        # Entry point for React app
│   ├── public/             # Static files like images, icons, etc.
│   ├── .env                # Environment variables for frontend (if needed)
│   ├── package.json        # Frontend dependencies and scripts
│   └── index.css           # Global CSS styles
│
└── README.md               # Project documentation (this file)
