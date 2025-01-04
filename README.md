
# Backend for Book Management System 📚

This repository contains the backend implementation for the Book Management System, providing APIs for user authentication, book management, comments, and wishlist functionality.

---

## Features 💡

- **User Authentication & Authorization**: Secure user login and registration.
- **Book Management**: CRUD operations for books.
- **Admin Controls**: Privileged operations for administrators.
- **Comment Feature**: Add comments to books.
- **Wishlist Feature**: Add or remove books from the wishlist.

---

## Environment Variables

To run this project, create a `.env` file in the root directory and add the following environment variables:

```bash
PORT=8000
MONGODB_URI=<your_mongodb_connection_string>
CORS_ORIGIN=*
ACCESS_TOKEN_SECRET=<your_access_token_secret>
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=<your_refresh_token_secret>
REFRESH_TOKEN_EXPIRY=10d
CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
CLOUDINARY_API_KEY=<your_cloudinary_api_key>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
```

---

## Run Locally

### Step 1: Clone the Repository

```bash
git clone <repository_url>
```

### Step 2: Navigate to the Project Directory

```bash
cd <project_directory>
```

### Step 3: Install Dependencies

```bash
npm install
```

### Step 4: Start the Server

```bash
npm run dev
```

The backend will run on `http://localhost:8000`.

---

## API Endpoints

### User Authentication

- `POST /auth/register`: Register a new user.
- `POST /auth/login`: Login with email and password.

### Books

- `GET /books`: Fetch all books.
- `POST /books`: Add a new book (Admin only).
- `PATCH /books/:id`: Update a book (Admin only).
- `DELETE /books/:id`: Delete a book (Admin only).

### Comments

- `POST /books/:id/comment`: Add a comment to a book.

### Wishlist

- `GET /books/toggleWishlist/:id`: Add/remove a book from the wishlist.

---

## Tech Stack

- **Server**: Node.js, Express.js
- **Database**: MongoDB, Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **File Storage**: Cloudinary for image uploads

---

## Deployment

Deploy your backend using any platform like Heroku, Render, or Vercel. Make sure to set all environment variables in the deployment platform.
