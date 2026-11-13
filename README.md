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
