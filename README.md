# Deployment and DevOps for MERN Applications

# MERN Expense Tracker
* A full-stack web application for tracking personal expenses, built with the MERN (MongoDB, Express.js, React, Node.js) stack. This application allows users to register, log in, add, view, update, and delete their financial transactions.


## Features
- User Authentication: Secure registration and login using JWT (JSON Web Tokens).

- Expense Management:

- Add new expenses with description, amount, and category.

- View a list of all recorded expenses.

- Edit existing expense details.

- Delete expenses.

- Expense Summary: Displays the total sum of all recorded expenses.

- Responsive Design: User interface adapts to different screen sizes (mobile, tablet, desktop).

- Client-side Routing: Seamless navigation between login, registration, and dashboard pages without full page reloads.

## Technologies Used
* This project leverages the MERN stack:

- MongoDB: A NoSQL database for storing user and expense data.

- Express.js: A fast, unopinionated, minimalist web framework for Node.js, used for building the RESTful API.

- React: A JavaScript library for building user interfaces, used for the frontend.

- React Hooks: useState, useEffect for state management and side effects.

- Client-side Routing: Implemented using URL hash (window.location.hash).

- Tailwind CSS: A utility-first CSS framework for rapid UI development.

- Boxicons: For icons in the authentication forms.

- Node.js: A JavaScript runtime environment, used for the backend server.*

## Other Key Libraries:

- mongoose: MongoDB object modeling for Node.js.

- bcryptjs: For hashing and salting passwords.

- jsonwebtoken: For implementing JWT-based authentication.

- dotenv: For loading environment variables from a .env file.

- cors: Node.js middleware for enabling Cross-Origin Resource Sharing.

- nodemon: (Development) Automatically restarts the Node.js server when file changes are detected.

## Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
Node.js (LTS version recommended)

npm (Node Package Manager, comes with Node.js)

MongoDB (local installation or a cloud service like MongoDB Atlas)

### Backend Setup
Clone the repository (or create the files manually as provided):
If you have the files in separate folders, ensure your backend project is in a directory (e.g., expense-tracker-backend).

Navigate to the backend directory:

cd expense-tracker-backend

Install backend dependencies:

npm install

Create a .env file:
In the root of your expense-tracker-backend directory, create a file named .env and add the following:

MONGO_URI=your_mongodb_connection_string_here
JWT_SECRET=a_very_strong_random_secret_key_for_jwt_signing
PORT=5000

Replace your_mongodb_connection_string_here with your MongoDB connection string (e.g., mongodb+srv://<username>:<password>@cluster0.abcde.mongodb.net/expense-tracker?retryWrites=true&w=majority).

Replace a_very_strong_random_secret_key_for_jwt_signing with a unique, long, and random string. This is crucial for security.

Start the backend server:

npm run server
// Or for production: npm start

The server will run on http://localhost:5000 (or the PORT you specified). You should see "MongoDB Connected..." and "Server running on port 5000" in your console.

### Frontend Setup
Clone the repository (or create the files manually as provided):
If you have the files in separate folders, ensure your frontend project is in a directory (e.g., expense-tracker-frontend).

Navigate to the frontend directory:

cd expense-tracker-frontend

Install frontend dependencies:

npm install

Start the React development server:

npm start

This will typically open the application in your browser at http://localhost:3000.

## Files Included

- `Week7-Assignment.md`: Detailed assignment instructions
- `.github/workflows/`: GitHub Actions workflow templates
- `deployment/`: Deployment configuration files and scripts
- `.env.example`: Example environment variable templates
- `monitoring/`: Monitoring configuration examples

## Requirements

- A completed MERN stack application from previous weeks
- Accounts on the following services:
  - GitHub
  - MongoDB Atlas
  - Render, Railway, or Heroku (for backend)
  - Vercel, Netlify, or GitHub Pages (for frontend)
- Basic understanding of CI/CD concepts

## Usage
Access the Application: Open your web browser and navigate to http://localhost:3000.

Register: If you're a new user, click on the "Register" button on the right side of the form. Fill in your desired username, email, and password, then click "Register".

Login: If you already have an account, click on the "Login" button. Enter your registered email and password, then click "Login".

Dashboard: Upon successful login, you will be redirected to the Dashboard.

Total Expenses: See a summary of your total spending.

Add New Expense: Use the form to input a description, amount, and category for a new expense, then click "Add Expense".

Your Expenses: View a table of all your recorded expenses.

Actions: Use the "Edit" (yellow pencil icon) and "Delete" (red trash can icon) buttons to manage individual expenses.

Logout: Click the "Logout" button to return to the authentication page.

## Folder Structure
The project is organized into backend and frontend directories.

```
├── expense-tracker-server/
│   ├── config/             # Database connection setup
│   │   └── db.js
│   ├── controllers/        # Business logic for routes
│   │   ├── authController.js
│   │   └── expenseController.js
│   ├── middleware/         # Custom middleware (e.g., authentication)
│   │   └── authMiddleware.js
│   ├── models/             # Mongoose schemas for data models
│   │   ├── User.js
│   │   └── Expense.js
│   ├── routes/             # API endpoints
│   │   ├── authRoutes.js
│   │   └── expenseRoutes.js
│   ├── .env                # Environment variables (sensitive info)
│   ├── package.json
│   └── server.js           # Main Express server file
│
└── expense-tracker-client/
    ├── public/
    ├── src/
    │   ├── App.js          # Main application component, handles routing
    │   ├── AuthForm.js     # Login and Registration form component
    │   ├── Dashboard.js    # Main dashboard component, manages expense state
    │   ├── ExpenseForm.js  # Component for adding new expenses
    │   ├── ExpenseList.js  # Component for displaying expenses table
    │   └── index.js        # React app entry point
    ├── package.json
    └── README.md           # This file
```

## Contributing
Contributions are welcome! If you have suggestions for improvements or find any bugs, please feel free to:

Fork the repository.

Create a new branch (git checkout -b feature/your-feature-name).

Make your changes.

Commit your changes (git commit -m 'Add new feature').

Push to the branch (git push origin feature/your-feature-name).

Open a Pull Request.
