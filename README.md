# 🗂️ MERN Task Management App

## 📌 Overview

The **MERN Task Management App** is a full-stack productivity web application built using the **MERN stack**:  
**MongoDB**, **Express.js**, **React.js**, and **Node.js**.

This app allows users to:
- Register and log in securely
- Manage tasks with full CRUD functionality
- Organize tasks by status, due date, and priority
- Access a responsive and clean UI
- Secure their data using JWT authentication

This project demonstrates a complete real-world implementation of modern MERN development, ideal for portfolio, internships, and production use.

---

## 🚀 Features

- **User Authentication**: Secure JWT-based registration and login  
- **Task Management**: Full CRUD operations (Create, Read, Update, Delete)  
- **User-Specific Tasks**: Users only manage their own tasks  
- **Task Properties**: Title, description, status, due date, priority  
- **Protected Routes**: Secure API with JWT middleware  
- **Responsive UI**: Built with Tailwind CSS for modern design  

---

## 🛠️ Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB + Mongoose
- JWT & bcrypt
- dotenv & cors

### Frontend
- React.js
- React Router
- Axios
- Tailwind CSS
- localStorage

---

## 📁 Project Structure

```
mern-task-manager/
├── client/
│   ├── public/
│   └── src/
│       ├── pages/
│       ├── components/
│       ├── App.js
│       └── index.js
├── server/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── server.js
│   └── .env
└── README.md
```

---

## 🚀 Quick Start

### 📦 Backend Setup

```bash
cd server
npm install
```

Create `.env` file:

```env
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_jwt_secret
PORT=5000
```

Start backend:

```bash
npm start
```

### 🌐 Frontend Setup

```bash
cd client
npm install
npm start
```

Frontend will run at `http://localhost:3000`

---

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` – Register new user
- `POST /api/auth/login` – Login user

### Tasks (Protected)
- `GET /api/tasks` – Fetch user’s tasks
- `POST /api/tasks` – Create a task
- `PUT /api/tasks/:id` – Update task
- `DELETE /api/tasks/:id` – Delete task

---

## 🔐 Features Overview

### ✅ Authentication
- Email + password auth
- JWT token generation & verification
- bcrypt password hashing
- Protected route middleware

### ✅ Task Features
- Add task (title, desc, date, priority, status)
- Edit and delete tasks
- Filter tasks by status
- Task UI using Tailwind CSS

---

## 🚀 Deployment Guide

### 🔹 Frontend (Vercel)

1. Push project to GitHub
2. Import repo in [vercel.com](https://vercel.com/)
3. Set root folder as `/client`
4. Add env: `VITE_API_BASE=https://your-backend.onrender.com`
5. Click **Deploy**

### 🔹 Backend (Render / Railway)

1. Push repo to GitHub
2. Go to [render.com](https://render.com/) or [railway.app](https://railway.app/)
3. Select `/server` as root
4. Add env vars:
   - `MONGO_URI`
   - `JWT_SECRET`
   - `PORT=5000`
5. Click **Deploy**

### 🔹 Database (MongoDB Atlas)

1. Create account at [mongodb.com](https://mongodb.com)
2. Create cluster → user → IP whitelist
3. Copy MongoDB URI
4. Paste in `.env` as `MONGO_URI`

---

## 🔧 Environment Variables

```env
# .env (Backend)
MONGO_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net/taskmanager
JWT_SECRET=super_secret_key
PORT=5000
```

```env
# .env (Frontend → via Vercel)
VITE_API_BASE=https://your-backend-url.onrender.com
```

---

## 🖼️ Screenshots

> Add these after deployment

- ✅ Login & Register Pages  
- ✅ Task List & Filter  
- ✅ Add/Edit Task Modal

---

## 🤝 Contributing

1. Fork the repo  
2. Create a new branch  
3. Commit changes with clear message  
4. Push to branch & create PR  

---

## 📄 License

Licensed under the MIT License.

---

## 🆘 Support

Feel free to [open an issue](https://github.com/your-username/mern-task-manager/issues) or reach out if you have questions.

---

**Happy Task Managing! ✅**
