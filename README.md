# News Website

A full-stack news website application built as a 3rd-year minor project collaboration.

## 📋 Table of Contents

- [Overview](#overview)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project is a comprehensive news website built with modern web technologies. It provides user authentication, news management, and a responsive user interface for browsing and managing news articles.

**Developed by:** Team Project (3rd Year Minor)

## 🛠️ Technology Stack

### Frontend
- **HTML5** - Markup structure
- **CSS3** - Styling and responsive design
- **Vanilla JavaScript** - Client-side logic and interactivity

### Backend
- **Node.js** - Server runtime environment
- **Express.js** - Web application framework (implied)
- **MongoDB** - NoSQL database
- **Environment Variables (.env)** - Configuration management

## 📁 Project Structure

```
news_website/
├── login_Server/                  # Main server folder
│   ├── server.js                  # Main entry point
│   ├── api/                       # API routes
│   │   └── user_api.js            # User authentication endpoints
│   ├── models/                    # Database models
│   │   └── user.js                # User schema
│   ├── config/                    # Configuration files
│   │   └── db.js                  # Database connection setup
│   └── .env                       # Environment variables (not committed)
├── README.md                      # Project documentation
└── package.json                   # Project dependencies
```

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0 or higher) - [Download here](https://nodejs.org/)
- **npm** (v6.0 or higher) - Comes with Node.js
- **MongoDB** - [Download here](https://www.mongodb.com/try/download/community) or use MongoDB Atlas
- **Git** - [Download here](https://git-scm.com/)

## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Shadan0786/news_website.git
   cd news_website
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Navigate to the server directory:**
   ```bash
   cd login_Server
   ```

## ⚙️ Configuration

### 1. Create Environment Variables File

Create a `.env` file in the `login_Server` directory with the following variables:

```env
# MongoDB Connection String
MONGODB_URI=mongodb://localhost:27017/news_website
# Or if using MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/news_website

# Server Configuration
PORT=5000
NODE_ENV=development

# Add other configuration variables as needed
```

**Important:** Never commit the `.env` file. It's already listed in `.gitignore`.

### 2. Database Setup

- **Local MongoDB:** Ensure MongoDB service is running on your machine
- **MongoDB Atlas:** Create a cluster and get your connection string from the Atlas dashboard

## 🎮 Running the Application

1. **Start the server:**
   ```bash
   node server.js
   ```

   Or if you have `nodemon` installed for development:
   ```bash
   npx nodemon server.js
   ```

2. **Access the application:**
   Open your browser and navigate to:
   ```
   http://localhost:5000
   ```

## 📡 API Documentation

### User Authentication Endpoints

All API endpoints are defined in `api/user_api.js`

#### User Model
The user data structure is defined in `models/user.js`

**Key user fields:**
- User ID
- Username
- Email
- Password (hashed)
- Created date
- Last login

### Example API Calls

```bash
# User Registration
POST /api/users/register
Content-Type: application/json

{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "secure_password"
}

# User Login
POST /api/users/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "secure_password"
}
```

## 🔧 Configuration Files

### db.js
Located in `login_Server/config/db.js`

This file handles MongoDB connection setup and initialization. Ensure your `MONGODB_URI` environment variable is properly set.

### server.js
Located in `login_Server/server.js`

Main entry point that starts the Express server and initializes all routes and middleware.

## 📝 Usage

1. **Register a new user** through the application interface
2. **Login** with your credentials
3. **Browse and manage** news articles
4. **Interact** with the news content

## 🐛 Troubleshooting

### MongoDB Connection Error
- Ensure MongoDB is running
- Verify your `MONGODB_URI` in the `.env` file
- Check MongoDB credentials if using Atlas

### Port Already in Use
- Change the `PORT` in your `.env` file
- Or kill the process using the current port

### Dependencies Not Installed
```bash
rm -rf node_modules package-lock.json
npm install
```

## 🤝 Contributing

This is a collaborative project. To contribute:

1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly
4. Submit a pull request with a clear description

## 📄 License

------

## 📧 Contact

For questions or issues, please reach out to the project maintainers.

---

