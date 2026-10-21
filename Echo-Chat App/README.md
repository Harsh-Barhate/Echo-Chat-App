# Full Stack Realtime Chat Application

A feature-rich realtime chat application built with Next.js. This project uses Next.js for both the frontend interface and backend API routes, while utilizing a dedicated custom Node.js/Express server specifically for handling realtime Socket.io connections.

## 🚀 Tech Stack

### Core & Full Stack
- **Framework:** [Next.js](https://nextjs.org/) (Frontend & API Routes)
- **Library:** [React](https://react.dev/)
- **Styling:** [TailwindCSS](https://tailwindcss.com/) & [DaisyUI](https://daisyui.com/)
- **State Management:** [Redux Toolkit](https://redux-toolkit.js.org/)
- **Database:** [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/)
- **Authentication:** [JWT](https://jwt.io/) & [bcryptjs](https://www.npmjs.com/package/bcryptjs)
- **Image Storage:** [Cloudinary](https://cloudinary.com/)
- **HTTP Client:** [Axios](https://axios-http.com/)
- **Icons:** [Lucide React](https://lucide.dev/)

### Realtime Service (Custom Server)
- **Runtime:** [Node.js](https://nodejs.org/)
- **Framework:** [Express](https://expressjs.com/)
- **Realtime Engine:** [Socket.io](https://socket.io/)

## 🛠️ Prerequisites

Before running the application, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18+ recommended)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas URI)
- A [Cloudinary](https://cloudinary.com/) account for image uploads

## ⚙️ Environment Variables

You need to configure environment variables for both the Next.js application and the realtime server.

### 1. Root Directory (`.env.local` or `.env`)
Create a `.env` file in the root directory:

```env
MONGODB_URI=your_mongodb_connection_string
NEXT_PUBLIC_SOCKET_URL=http://localhost:4000
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### 2. Server Directory (`server/.env`)
Create a `.env` file in the `server` directory:

```env
PORT=4000
CLIENT_URL=http://localhost:3000
JWT_SECRET=your_jwt_secret_key
```

> **Note:** Ensure `NEXT_PUBLIC_SOCKET_URL` in the root matches the `PORT` in the server config, and `CLIENT_URL` in the server matches your Next.js frontend URL.

## 📦 Installation

### 1. Install Root Dependencies (Next.js App)
```bash
npm install
# or
yarn install
```

### 2. Install Server Dependencies (Realtime Service)
```bash
cd server
npm install
# or
yarn install
```

## 🏃‍♂️ Running the Application

You need to run both the realtime service and the main Next.js application concurrently.

### 1. Start the Realtime Service (Socket.io)
Open a terminal and run:

```bash
cd server
npm start
# or for development with nodemon
npm run dev
```
The socket server will start on port `4000` (or your defined port).

### 2. Start the Main Application (Next.js)
Open a new terminal in the root directory and run:

```bash
npm run dev
# or
yarn dev
```
The application (Frontend + APIs) will be available at [http://localhost:3000](http://localhost:3000).

## ✨ Features

- **Realtime Messaging:** Instant message delivery using Socket.io.
- **User Authentication:** Secure signup and login with JWT.
- **Persistent Chat:** Messages are stored in MongoDB.
- **Ephemeral Messages:** Toggle ephemeral mode for temporary conversations.
- **Media Sharing:** Upload and share images via Cloudinary.
- **Online Status:** See who is currently online.
- **Typing Indicators:** Realtime feedback when users are typing.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
