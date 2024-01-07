
Course Management System
This repository contains the code for a Course Management System built with Node.js, Express, MongoDB, and JWT authentication. The system allows both admins and users to interact with courses.

Prerequisites
Node.js
MongoDB
Installation
Clone the repository:

git clone https://github.com/your-username/course-management-system.git
Install dependencies:

cd course-management-system
npm install
Set up MongoDB:

Ensure MongoDB is installed and running.
Update the MongoDB connection URI in app.js file:
javascript
mongoose.connect('your-mongodb-connection-uri', { useNewUrlParser: true, useUnifiedTopology: true, dbName: "courses" });
Usage
Start the server:

npm start
The server will start running at http://localhost:3000.

API Endpoints
Admin Routes
POST /admin/signup

Create a new admin account.
POST /admin/login

Login for admin.
POST /admin/courses

Create a new course (authentication required).
PUT /admin/courses/:courseId

Update a specific course (authentication required).
GET /admin/courses

Get all courses (authentication required).
User Routes
POST /users/signup

Create a new user account.
POST /users/login

Login for users.
GET /users/courses

Get all published courses available for users (authentication required).
POST /users/courses/:courseId

Purchase a course for the user (authentication required).
GET /users/purchasedCourses

Get all purchased courses by the user (authentication required).
Authentication
JSON Web Tokens (JWT) are used for authentication.
Admins and users receive a token upon login, which is then used to access protected routes.
Important Note
This system is for educational purposes only. Ensure that the provided MongoDB connection URL is secure and use it responsibly.
Feel free to contribute or report issues by creating a pull request or raising an issue in the repository. Thank you for your interest!
