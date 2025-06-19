# MERN Task Manager - Setup Guide

This guide will help you set up and run the MERN Task Manager application on your local machine.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **MongoDB Atlas account** (for cloud database) - [Sign up here](https://www.mongodb.com/atlas)

## Step 1: Clone the Repository

```bash
git clone <your-repository-url>
cd mern-task-manager
```

## Step 2: Set Up MongoDB Atlas

1. Go to [MongoDB Atlas](https://www.mongodb.com/atlas) and create a free account
2. Create a new cluster (the free tier is sufficient)
3. Create a database user with read/write permissions
4. Get your connection string from the "Connect" button
5. Replace `<username>`, `<password>`, and `<cluster-url>` with your actual values

## Step 3: Backend Setup

1. Navigate to the server directory:
```bash
cd server
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the server directory:
```bash
cp env.example .env
```

4. Edit the `.env` file with your MongoDB connection string and JWT secret:
```env
MONGO_URI=mongodb+srv://your_username:your_password@your_cluster.mongodb.net/taskmanager
JWT_SECRET=your_super_secret_jwt_key_here_make_it_long_and_random
PORT=5000
```

5. Start the server:
```bash
npm start
```

The backend should now be running on `http://localhost:5000`

## Step 4: Frontend Setup

1. Open a new terminal and navigate to the client directory:
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

The frontend should now be running on `http://localhost:3000`

## Step 5: Test the Application

1. Open your browser and go to `http://localhost:3000`
2. You should be redirected to the login page
3. Click "create a new account" to register
4. After registration, you'll be logged in and can start creating tasks

## Troubleshooting

### Common Issues

1. **MongoDB Connection Error**
   - Make sure your MongoDB Atlas cluster is running
   - Check that your connection string is correct
   - Ensure your IP address is whitelisted in MongoDB Atlas

2. **Port Already in Use**
   - If port 5000 is in use, change the PORT in your `.env` file
   - If port 3000 is in use, React will automatically suggest an alternative port

3. **CORS Errors**
   - The backend is configured to allow requests from `http://localhost:3000`
   - If you're using a different port, update the CORS configuration in `server/server.js`

4. **JWT Token Issues**
   - Make sure your JWT_SECRET is a long, random string
   - Clear your browser's localStorage if you encounter token issues

### Development Commands

**Backend:**
```bash
cd server
npm start          # Start production server
npm run dev        # Start development server with nodemon
```

**Frontend:**
```bash
cd client
npm start          # Start development server
npm run build      # Build for production
npm test           # Run tests
```

## Environment Variables Reference

### Backend (.env)
```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/taskmanager
JWT_SECRET=your_super_secret_jwt_key_here
PORT=5000
```

### Frontend (.env)
```env
REACT_APP_API_URL=http://localhost:5000/api
```

## API Endpoints

Once the server is running, you can test the API endpoints:

- `GET http://localhost:5000/api/health` - Health check
- `POST http://localhost:5000/api/auth/register` - User registration
- `POST http://localhost:5000/api/auth/login` - User login
- `GET http://localhost:5000/api/tasks` - Get all tasks (requires auth)
- `POST http://localhost:5000/api/tasks` - Create task (requires auth)
- `PUT http://localhost:5000/api/tasks/:id` - Update task (requires auth)
- `DELETE http://localhost:5000/api/tasks/:id` - Delete task (requires auth)

## Next Steps

After successful setup, you can:

1. **Customize the UI** - Modify the Tailwind CSS classes in the React components
2. **Add Features** - Implement additional features like task categories, reminders, etc.
3. **Deploy** - Follow the deployment instructions in the main README.md
4. **Add Tests** - Write unit and integration tests for both frontend and backend

## Support

If you encounter any issues during setup, please:

1. Check the troubleshooting section above
2. Ensure all prerequisites are installed correctly
3. Verify your MongoDB Atlas configuration
4. Check the browser console and server logs for error messages

For additional help, refer to the main README.md file or create an issue in the repository. 