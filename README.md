# 📸 MERN Post

A simple full-stack **image-post app** built with the MERN stack. Users can upload an image with a caption and see all posts in a scrolling feed. Images are stored on **ImageKit** and post data is stored in **MongoDB**.

## ✨ Features

- Create a post with an image and a caption
- View all posts in a clean feed
- Image upload handled in memory with **Multer** and sent to **ImageKit** cloud storage
- Post data (image URL + caption) saved in **MongoDB** via Mongoose
- Client-side routing with React Router

## 🛠️ Tech Stack

| Layer    | Technologies                                   |
| -------- | ---------------------------------------------- |
| Frontend | React (Vite), React Router DOM, Axios, CSS     |
| Backend  | Node.js, Express, Multer, CORS, dotenv         |
| Database | MongoDB, Mongoose                              |
| Storage  | ImageKit                                       |

## 📁 Project Structure

```
Mern_post/
├── backend/
│   ├── server.js                  # Starts the server and connects to the DB
│   └── src/
│       ├── app.js                 # Express app and API routes
│       ├── db/db.js               # MongoDB connection
│       ├── models/post.model.js   # Post schema (image, caption)
│       └── services/storage.services.js  # ImageKit upload helper
└── frontend/
    └── src/
        ├── main.jsx
        ├── App.jsx                # Routes
        ├── index.css
        └── pages/
            ├── CreatePost.jsx     # Upload form
            └── Feed.jsx           # Posts feed
```

## 🔌 API Endpoints

| Method | Endpoint       | Description                                                        |
| ------ | -------------- | ------------------------------------------------------------------ |
| POST   | `/create-post` | Upload an image (`image`) and a `caption` (multipart/form-data)    |
| GET    | `/posts`       | Fetch all posts                                                    |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- A [MongoDB](https://www.mongodb.com/) database (local or Atlas)
- An [ImageKit](https://imagekit.io/) account (for the private key)

### 1. Clone the repository

```bash
git clone https://github.com/Nadeem882/Mern_post.git
cd Mern_post
```

### 2. Set up the backend

```bash
cd backend
npm install
```

Create a `.env` file inside `backend/`:

```env
MONGO_URI=your_mongodb_connection_string
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
```

Start the server (runs on **http://localhost:3**):

```bash
node server.js
```

### 3. Set up the frontend

Open a new terminal:

```bash
cd frontend
npm install
npm run dev
```

## 🖥️ Usage

1. Go to `http://localhost:5173/create-post`
2. Choose an image, write a caption, and click **Submit**
3. You'll be redirected to `http://localhost:5173/feed` where all posts are shown
