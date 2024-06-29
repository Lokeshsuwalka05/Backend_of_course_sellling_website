# Course Selling Website Backend

This repository contains the backend code for a course selling website. The backend is built using Express.js and MongoDB, and includes features for both administrators and users.

## Features

### Admin
- Sign up
- Login
- Create courses
- Update courses
- View all courses

### Users
- Sign up
- Login
- View published courses
- Purchase courses
- View purchased courses

## Technologies Used
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT for authentication
- Bcrypt for password hashing

## Installation

1. Clone the repository
   
    git clone https://github.com/yourusername/Backend_of_course_sellling_website.git
    ```
2. Navigate to the project directory
  
    cd course-selling-backend
    ```
3. Install dependencies
   
    npm install
    ```

## Configuration

1. Create a `.env` file in the root of the project and add the following variables:
   
    SECRET=your_jwt_secret
    MONGODB_URI=your_mongodb_connection_string
    ```

## Running the Application

1. Start the server
    
    npm start
    ```
2. The server will be running on `http://localhost:3000`.

## API Endpoints

### Admin Routes

- **Sign Up**  
  `POST /admin/signup`  
  Request body: `{ "username": "admin", "password": "password" }`

- **Login**  
  `POST /admin/login`  
  Request headers: `{ "username": "admin", "password": "password" }`

- **Create Course**  
  `POST /admin/courses`  
  Request body: `{ "title": "Course Title", "description": "Course Description", "price": 100, "imageLink": "http://image.url", "published": true }`
  
- **Update Course**  
  `PUT /admin/courses/:courseId`  
  Request body: `{ "title": "Updated Course Title", "description": "Updated Course Description", "price": 150, "imageLink": "http://updated.image.url", "published": false }`
  
- **View All Courses**  
  `GET /admin/courses`

### User Routes

- **Sign Up**  
  `POST /users/signup`  
  Request body: `{ "username": "user", "password": "password" }`

- **Login**  
  `POST /users/login`  
  Request headers: `{ "username": "user", "password": "password" }`

- **View Published Courses**  
  `GET /users/courses`

- **Purchase Course**  
  `POST /users/courses/:courseId`

- **View Purchased Courses**  
  `GET /users/purchasedCourses`

## Authentication

This application uses JWT for authentication. Include the JWT token in the `Authorization` header as follows:
