📌 Short URL Generator – Node.js & MongoDB Project
🔹 Project Overview

This project is a Short URL Generator built using Node.js, Express.js, and MongoDB. The main objective of the project is to convert long, complex URLs into short, unique, and easily shareable links. When a user accesses the generated short URL, the application automatically redirects them to the original long URL.

The project follows a clean and modular backend architecture, separating concerns into routes, controllers, models, and database connection layers. It demonstrates real-world backend development practices such as REST API design, database integration, and URL redirection handling.

🔹 Problem Statement

Long URLs are difficult to share, remember, and manage. This project solves that problem by generating short identifiers for long URLs and storing them in a database. The short identifier can later be used to retrieve and redirect users to the original URL.

🔹 Features

Generate a unique short URL for any valid long URL

Store URL mappings securely in MongoDB

Redirect users from short URL to original URL

RESTful API design using Express.js

Clean folder structure using MVC architecture

Automatic database timestamps for tracking data creation

Error handling for invalid or missing URLs

🔹 Tech Stack

Backend: Node.js

Framework: Express.js

Database: MongoDB

ODM: Mongoose

Unique ID Generator: shortid

Development Tool: Nodemon

🔹 Project Architecture

The project follows a structured backend design:

index.js – Entry point of the application, initializes server and middleware

connect.js – Handles MongoDB connection logic

models/ – Contains Mongoose schema and model definitions

controllers/ – Contains business logic for URL generation

routes/ – Handles API routing and request mapping

This separation ensures better readability, scalability, and maintainability.

🔹 API Endpoints
1️⃣ Generate Short URL

Endpoint:

POST /url


Request Body:

{
  "url": "https://example.com"
}


Response:

{
  "id": "abc123"
}

2️⃣ Redirect to Original URL

Endpoint:

GET /:shortId


Example:

http://localhost:8002/abc123


➡️ Redirects to the original URL stored in the database.

🔹 Database Design

Each URL document stored in MongoDB contains:

shortId – Unique generated identifier

redirectURL – Original long URL

visitHistory – Reserved for future analytics

createdAt & updatedAt – Automatically managed timestamps

🔹 How to Run the Project Locally

Clone the repository

git clone https://github.com/aarti12217444/short-url.git


Navigate to the project folder

cd short-url


Install dependencies

npm install


Start the server

npm start


Server will run on

http://localhost:8002

🔹 Learning Outcomes

Through this project, I gained hands-on experience with:

Building REST APIs using Express.js

Connecting and working with MongoDB using Mongoose

Designing backend architecture using MVC principles

Handling HTTP requests and responses

Implementing URL redirection logic

Managing Git and GitHub for version control

🔹 Future Enhancements

URL visit count and analytics

Custom alias support

URL expiration feature

User authentication and dashboard

Rate limiting and security enhancements

🔹 Conclusion

This project demonstrates a complete backend workflow from API creation to database interaction and URL redirection. It reflects practical backend development skills and can be easily extended into a full-scale URL management system.
