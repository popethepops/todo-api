# ✅ Todo API

A simple Node.js + Express API for user registration, login, and managing todos. MongoDB is used as the database, and Postman/Hoppscotch for testing the endpoints.

---

## 🚀 Project Setup (Run Locally)

### 1. Clone this repository
```bash
git clone https://github.com/your-username/todo-api.git
cd todo-api
```

### 2. Install dependencies
```bash
npm install
```

### 3. Create a `.env` file
Create a `.env` file in the root and add:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

### 4. Start the server
```bash
npm run dev
```

> Server will run at: `http://localhost:5000`

---

## 🧪 API Documentation

All routes accept and return JSON unless specified otherwise.

### 🔐 Auth Routes

#### `POST /auth/register`
- Register a new user.
- Body:
```json
{
  "email": "user@example.com",
  "password": "yourpassword"
}
```

#### `POST /auth/login`
- Login with credentials.
- Body:
```json
{
  "email": "user@example.com",
  "password": "yourpassword"
}
```

---

### 📝 Todo Routes

> 🔐 All todo routes require a valid JWT in the `Authorization` header.

#### `GET /todos`
- Get all todos for the authenticated user.

#### `POST /todos`
- Create a new todo.
- Body:
```json
{
  "title": "Buy groceries",
  "description": "Milk, Eggs, Bread"
}
```

#### `PUT /todos/:id`
- Update an existing todo by ID.

#### `DELETE /todos/:id`
- Delete a todo by ID.

---

## 🛠 Built With

- Node.js
- Express
- MongoDB
- Mongoose
- bcryptjs
- dotenv


Postman
https://rogerpurnomo-5859712.postman.co/workspace/Personal-Workspace~62ff0395-d9b1-4f87-89f2-e23c837d9f66/request/47395504-455d038d-2596-46e7-834b-e7a398e30bbd?action=share&source=copy-link&creator=47395504
