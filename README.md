# Personal Notes App - Backend

## Technology Stack

- Node.js + Express
- MongoDB (with Mongoose)
- JWT Authentication
- ES Modules

## Features

- User Authentication (Register, Login)
- JWT-based Authentication
- Protected Routes for Notes
- CRUD Operations for Notes (Create, Read, Update, Delete)
- Notes are user-specific


## Setup Instructions

1. Clone this repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file in the root directory with the following variables:
   ```
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/notes_app
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRES_IN=30d
   ```
4. Start the server:
   ```
   npm start
   ```
   or for development:
   ```
   npm run dev
   ```

## API Endpoints

### User Routes
- `POST /api/users/register` - Register a new user
- `POST /api/users/login` - Login an existing user
- `GET /api/users/profile` - Get user profile (protected)

### Note Routes
- `GET /api/notes` - Get all notes for logged in user (protected)
- `POST /api/notes` - Create a new note (protected)
- `GET /api/notes/:id` - Get a specific note by ID (protected)
- `PUT /api/notes/:id` - Update a specific note (protected)
- `DELETE /api/notes/:id` - Delete a specific note (protected)

## Authentication

The application uses JWT for authentication. When a user registers or logs in, a JWT token is generated and returned to the client. This token should be included in the Authorization header of subsequent requests as a Bearer token:

```
Authorization: Bearer <token>
```
