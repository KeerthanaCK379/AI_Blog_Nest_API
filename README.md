# AI BlogNest API 🤖

AI BlogNest API is an AI-powered RESTful backend application for creating, managing, and enhancing blog content. It provides secure user authentication, complete blog CRUD operations, and AI-powered content generation and summarization.

The project is developed using Node.js, Express.js, MongoDB, Mongoose, JWT, bcrypt, and Gemini AI, following an MVC architecture.

---

## 📌 Project Overview

AI BlogNest API provides a backend platform where users can securely manage their blog posts and use AI-powered features to generate and summarize content.

The application allows users to:

- Register and create an account
- Login securely using authentication
- Access protected API routes
- Create blog posts
- View all blog posts
- View individual blog posts
- Update blog posts
- Delete blog posts
- Generate blog content using Gemini AI
- Summarize blog content using Gemini AI

The API follows RESTful API principles and can be integrated with web or mobile frontend applications.

---

## 🎯 Objectives

The main objectives of AI BlogNest API are:

1. To develop a secure RESTful backend for blog management.
2. To implement user authentication using JWT.
3. To securely store passwords using bcrypt.
4. To provide complete CRUD operations for blogs.
5. To integrate Gemini AI for blog content generation.
6. To provide AI-powered blog summarization.
7. To implement a structured MVC architecture.
8. To create a maintainable and scalable backend application.

---

## ✨ Features

### 👤 User Authentication

- User registration
- User login
- Password hashing using bcrypt
- JWT-based authentication
- Protected API routes
- User profile access

### 📝 Blog Management

- Create blog posts
- View all blog posts
- View individual blog posts
- Update blog posts
- Delete blog posts
- Complete CRUD operations

### 🤖 AI Features

- AI-powered blog content generation
- AI-powered blog summarization
- Gemini AI integration

### 🔐 Security

- Password hashing using bcrypt
- JWT authentication
- Protected routes
- Environment variables for sensitive information

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Node.js | Backend runtime environment |
| Express.js | REST API framework |
| MongoDB | Database |
| Mongoose | MongoDB object modelling |
| JWT | User authentication |
| bcrypt | Password hashing |
| Gemini AI | AI content generation and summarization |
| JavaScript | Programming language |
| Thunder Client | API testing |

---

## 🏗️ Architecture

The project follows an MVC-based backend architecture.

```text
                         Client
                           |
                           v
                    Express.js API
                           |
             +-------------+-------------+
             |             |             |
             v             v             v
        Auth Routes    Blog Routes    AI Routes
             |             |             |
             v             v             v
        Controllers    Controllers    Gemini AI
             |             |
             v             v
           Models ---> MongoDB
````

---

## 🔄 Application Workflow

```text
User
 |
 +---- Register
 |       |
 |       v
 |   Account Created
 |
 +---- Login
 |       |
 |       v
 |   JWT Token
 |
 v
Authenticated User
 |
 +---- Create Blog
 |
 +---- View Blogs
 |
 +---- Update Blog
 |
 +---- Delete Blog
 |
 +---- AI Features
          |
          +---- Generate Blog
          |
          +---- Summarize Blog
```

---

## 🔐 Authentication

AI BlogNest API uses JSON Web Token (JWT) authentication to protect user-specific resources.

During registration, passwords are securely hashed using bcrypt.

During login, the user is authenticated and a JWT token is generated. The token is then used to access protected API routes.

```text
Register / Login
       |
       v
Authentication
       |
       v
JWT Token Generated
       |
       v
Authenticated Request
       |
       v
Protected API Route
```

---

## 🤖 Gemini AI Integration

AI BlogNest API integrates Gemini AI to provide intelligent blog-related functionality.

### ✍️ AI Blog Generation

The `/api/ai/generate-blog` endpoint can be used to generate blog content based on a user-provided topic or prompt.

### 📝 AI Summarization

The `/api/ai/summarize` endpoint can be used to generate a concise summary of blog content.

### AI Workflow

```text
User Prompt
    |
    v
AI API Endpoint
    |
    v
Gemini AI
    |
    v
Generated / Summarized Content
    |
    v
API Response
```

---

## 🔗 API Endpoints

### 👤 Authentication

| Method | Endpoint             | Description                    |
| ------ | -------------------- | ------------------------------ |
| POST   | `/api/auth/register` | Register a new user            |
| POST   | `/api/auth/login`    | Login user                     |
| GET    | `/api/auth/profile`  | Get authenticated user profile |

### 📝 Blogs

| Method | Endpoint         | Description         |
| ------ | ---------------- | ------------------- |
| POST   | `/api/blogs`     | Create a new blog   |
| GET    | `/api/blogs`     | Get all blogs       |
| GET    | `/api/blogs/:id` | Get a specific blog |
| PUT    | `/api/blogs/:id` | Update a blog       |
| DELETE | `/api/blogs/:id` | Delete a blog       |

### 🤖 AI

| Method | Endpoint                | Description                     |
| ------ | ----------------------- | ------------------------------- |
| POST   | `/api/ai/generate-blog` | Generate blog content using AI  |
| POST   | `/api/ai/summarize`     | Summarize blog content using AI |

---

## 🧪 API Testing

The API was tested using Thunder Client.

The following functionalities were tested:

* User registration
* User login
* JWT authentication
* User profile
* Blog creation
* Blog retrieval
* Individual blog retrieval
* Blog update
* Blog deletion
* AI blog generation
* AI summarization

Postman can also be used to test the API endpoints.

---

## 📂 Project Structure

```text
ai-blognest-api/
│
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   └── server.js
│
├── .env.example
├── package.json
├── package-lock.json
├── README.md
└── ...
```

---

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed on your system:

* Node.js
* npm
* MongoDB / MongoDB Atlas
* Gemini API key

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Open the Project Folder

```bash
cd ai-blognest-api
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Create the Environment File

Create a `.env` file in the project root directory.

Add the required environment variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=your_gemini_model
```

### 5. Start the Development Server

```bash
npm run dev
```

The API will start on the configured port.

---

## 🔑 Environment Variables

| Variable         | Description                             |
| ---------------- | --------------------------------------- |
| `PORT`           | Port used by the backend server         |
| `MONGO_URI`      | MongoDB connection string               |
| `JWT_SECRET`     | Secret key used for JWT authentication  |
| `GEMINI_API_KEY` | Gemini AI API key                       |
| `GEMINI_MODEL`   | Gemini AI model used by the application |

> ⚠️ Do not upload your `.env` file or expose your API keys, MongoDB credentials, or JWT secret on GitHub.

---

## 🗄️ Database

The project uses MongoDB as its database.

Mongoose is used to define schemas and communicate with MongoDB.

The database stores application data such as:

* User information
* Blog posts
* Blog content
* Timestamps and related information

MongoDB Atlas can be used for cloud-based database hosting.

---

## 🧩 MVC Architecture

The project follows the Model-View-Controller architecture.

### Model

Handles database schemas and communication with MongoDB.

### View

The project is primarily a RESTful backend API. API responses provide the required data to the client.

### Controller

Handles application logic and processes API requests.

### Routes

Defines API endpoints and connects requests to the appropriate controllers.

### Middleware

Handles authentication and other request-processing operations.

---

## 🎥 Demo Video

Watch the complete project demonstration:

[▶️ Watch AI BlogNest API Demo Video](https://drive.google.com/file/d/1oz4PqEsmLTC8HROD9TSGdw_HmPkJwtT5/view?usp=drivesdk)

---

## 📄 Project Documentation

The complete project documentation includes:

* Project introduction
* Project objectives
* Technologies used
* System architecture
* Database integration
* Authentication
* API implementation
* Gemini AI integration
* API testing
* Screenshots
* Results
* Project workflow

---

## 📊 Project Status

| Module                | Status        |
| --------------------- | ------------- |
| User Registration     | ✅ Completed   |
| User Login            | ✅ Completed   |
| JWT Authentication    | ✅ Completed   |
| User Profile          | ✅ Completed   |
| Blog Creation         | ✅ Completed   |
| Blog Retrieval        | ✅ Completed   |
| Blog Update           | ✅ Completed   |
| Blog Deletion         | ✅ Completed   |
| MongoDB Integration   | ✅ Completed   |
| Gemini AI Integration | ✅ Implemented |
| AI Blog Generation    | ✅ Implemented |
| AI Summarization      | ✅ Implemented |
| API Testing           | ✅ Completed   |
| Documentation         | ✅ Completed   |
| Demo Video            | ✅ Prepared    |

---

## 🚀 Future Enhancements

The project can be extended with additional features such as:

* User roles and permissions
* Blog categories and tags
* Search and filtering
* Likes and comments
* Image upload
* Pagination
* User dashboard
* Blog analytics
* Advanced AI writing assistance
* Frontend web application

---

## 👥 Team

**Project Name:** AI BlogNest API

**Project Type:** AI-Powered RESTful Blog Management API

---

## ⭐ Conclusion

AI BlogNest API demonstrates the practical implementation of RESTful API development, secure authentication, database management, CRUD operations, and AI integration.

The project combines modern backend technologies with Gemini AI to provide an intelligent and extensible blog management platform.

---

## 📜 License

This project is developed for educational and academic purposes.
