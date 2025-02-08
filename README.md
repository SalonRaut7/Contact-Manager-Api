# Contact Manager API

## 📌 Introduction
The **Contact Manager API** is a RESTful API built with Node.js and Express that allows users to manage their contacts. It provides authentication using JWT and enables users to perform CRUD operations on contacts.

## 🚀 Features
- **User Authentication** (Register, Login, JWT-based Authentication)
- **Manage Contacts** (Create, Read, Update, Delete)
- **Secure API Endpoints** (Protected Routes for Logged-in Users)
- **MongoDB Database** (Mongoose for Schema Management)

## 🛠️ Technologies Used
- **Node.js**
- **Express.js**
- **MongoDB & Mongoose**
- **JWT (JSON Web Token) Authentication**
- **bcrypt for Password Hashing**

## 📂 Project Structure
📦 Contact-Manager-Api
┣ 📂 config ┃ ┗ 📜 dbConnection.js ┣ 📂 controllers ┃ ┣ 📜 contactController.js ┃ ┗ 📜 userController.js ┣ 📂 middleware ┃ ┣ 📜 errorHandler.js ┃ ┗ 📜 validateTokenHandler.js ┣ 📂 models ┃ ┣ 📜 contactModel.js ┃ ┗ 📜 userModel.js ┣ 📂 routes ┃ ┣ 📜 contactRoutes.js ┃ ┗ 📜 userRoutes.js ┣ 📜 .env (Environment Variables - Not Included in Repo) ┣ 📜 .gitignore ┣ 📜 constants.js ┣ 📜 package.json ┣ 📜 package-lock.json ┣ 📜 server.js ┗ 📜 README.md


## 🔧 Installation & Setup
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/SalonRaut7/Contact-Manager-Api.git
cd Contact-Manager-Api
```
### 2️⃣ Install Dependencies
```sh
npm install
```
### 3️⃣ Configure Environment Variables
Create a .env file in the root directory and add the following:
```sh
PORT=5000
CONNECTION_STRING=your_mongodb_connection_string
ACCESS_TOKEN_SECRET=your_secret_key
```
### 4️⃣ Start the Server
Create a .env file in the root directory and add the following:
```sh
npm run dev
```

🔑 Authentication
The API uses JWT authentication.
For protected routes, include a Bearer Token in the request header:
```sh
Authorization: Bearer <your_token>
```

## 🔗 API Endpoints

### 🟢 Authentication
| Method | Endpoint               | Description                      |
|--------|------------------------|----------------------------------|
| POST   | `/api/users/register`  | Register a new user              |
| POST   | `/api/users/login`     | Log in and get a JWT token       |
| GET    | `/api/users/current`   | Get current logged-in user info  |

### 📞 Contact Management
| Method | Endpoint               | Description                      |
|--------|------------------------|----------------------------------|
| GET    | `/api/contacts`        | Get all contacts (Protected)     |
| POST   | `/api/contacts`        | Create a new contact (Protected) |
| GET    | `/api/contacts/:id`    | Get a specific contact (Protected) |
| PUT    | `/api/contacts/:id`    | Update a contact (Protected)     |
| DELETE | `/api/contacts/:id`    | Delete a contact (Protected)     |






