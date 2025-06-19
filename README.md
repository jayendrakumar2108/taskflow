# MERN Task Management App

A full-featured task management application built with the MERN stack (MongoDB, Express.js, React.js, Node.js) with user authentication and CRUD operations for tasks.

## 🚀 Features

- **User Authentication**: Secure JWT-based authentication with registration and login
- **Task Management**: Full CRUD operations for tasks (Create, Read, Update, Delete)
- **User-Specific Tasks**: Each user can only see and manage their own tasks
- **Task Properties**: Title, description, status (todo, in-progress, done), due date, priority
- **Responsive Design**: Clean and modern UI with Tailwind CSS
- **Protected Routes**: Secure API endpoints with JWT middleware

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **bcrypt** - Password hashing
- **cors** - Cross-origin resource sharing
- **dotenv** - Environment variables

### Frontend
- **React.js** - JavaScript library for building user interfaces
- **React Router** - Client-side routing
- **Axios** - HTTP client for API calls
- **Tailwind CSS** - Utility-first CSS framework
- **localStorage** - Client-side storage for JWT tokens

## 📁 Project Structure

```
mern-task-manager/
├── client/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Login.js
│   │   │   ├── Register.js
│   │   │   └── Home.js
│   │   ├── components/
│   │   │   ├── TaskForm.js
│   │   │   ├── TaskList.js
│   │   │   └── TaskItem.js
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── tailwind.config.js
├── server/
│   ├── models/
│   │   ├── User.js
│   │   └── Task.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   └── taskRoutes.js
│   ├── middleware/
│   │   └── auth.js
│   ├── .env
│   ├── package.json
│   └── server.js
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MongoDB Atlas account (for cloud database)

### Backend Setup

1. Navigate to the server directory:
```bash
cd server
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the server directory:
```env
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
```

4. Start the server:
```bash
npm start
```

The backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to the client directory:
```bash
cd client
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The frontend will run on `http://localhost:3000`

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### Tasks
- `GET /api/tasks` - Get all tasks for authenticated user
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task

## 🎨 Features Overview

### Authentication
- Secure user registration with email validation
- Password hashing using bcrypt
- JWT token generation and verification
- Protected routes middleware

### Task Management
- Create tasks with title, description, status, due date, and priority
- View all tasks in a clean, organized list
- Update task details and status
- Delete tasks with confirmation
- Filter tasks by status (todo, in-progress, done)

### User Interface
- Responsive design that works on desktop and mobile
- Clean, modern UI with Tailwind CSS
- Intuitive navigation between pages
- Form validation and error handling
- Loading states and user feedback

## 🚀 Deployment

### Frontend (Vercel)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Deploy with default settings
4. Update the API base URL in the frontend to point to your deployed backend

### Backend (Render/Railway)
1. Push your code to GitHub
2. Connect your repository to Render or Railway
3. Set environment variables (MONGO_URI, JWT_SECRET)
4. Deploy the application

### Database (MongoDB Atlas)
1. Create a free MongoDB Atlas account
2. Create a new cluster
3. Get your connection string
4. Add it to your backend environment variables

## 🔧 Environment Variables

### Backend (.env)
```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/taskmanager
JWT_SECRET=your_super_secret_jwt_key_here
PORT=5000
```

## 📸 Screenshots

*Screenshots will be added after deployment*

- Login/Register pages
- Dashboard with task list
- Task creation form
- Task editing interface

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License.

## 🆘 Support

If you encounter any issues or have questions, please open an issue on GitHub or contact the development team.

---

**Happy Task Managing! 🎯** 