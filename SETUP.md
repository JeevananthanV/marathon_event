# StrideForge Events — Marathon Event Setup Guide

Welcome to the **StrideForge Marathon Event Management System** setup guide. This document provides step-by-step instructions for running the React frontend and Node.js + MongoDB backend.

- **GitHub Repository**: [https://github.com/JeevananthanV/marathon_event](https://github.com/JeevananthanV/marathon_event)
- **Author**: Jeevananthan V

---

## 📋 System Prerequisites

- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher
- **MongoDB**: MongoDB Atlas connection URI or local MongoDB daemon
- **Git**: v2.30.0 or higher

---

## 📥 1. Clone the Repository

```bash
git clone https://github.com/JeevananthanV/marathon_event.git
cd marathon_event
```

---

## ⚙️ 2. Environment Variables Configuration

### Backend Environment (`marathon-be/.env`)

```env
PORT=5000
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=strideforge_secret_jwt_token_2026
CLIENT_URL=http://localhost:5173
```

### Frontend Environment (`marathon-fe/.env`)

```env
VITE_API_URL=http://localhost:5000/api
```

---

## 📦 3. Install Dependencies

```bash
# 1. Install Backend Dependencies
cd marathon-be
npm install

# 2. Install Frontend Dependencies
cd ../marathon-fe
npm install
cd ..
```

---

## 🚀 4. Running the Application Locally

### Terminal 1: Backend API (Port 5000)

```bash
cd marathon-be
npm run dev
```
API starts at: `http://localhost:5000`
- Health check: `http://localhost:5000/api/health`

### Terminal 2: Frontend Client (Port 5173)

```bash
cd marathon-fe
npm run dev
```
Frontend starts at: `http://localhost:5173`

---

## 🏗️ 5. Production Build

```bash
cd marathon-fe
npm run build
```
Compiled output will be in `marathon-fe/dist/`.

---

## 🛠️ Troubleshooting

- **MongoDB Connection Error**: Check your IP whitelist on MongoDB Atlas (allow current IP or `0.0.0.0/0`).
- **CORS Block**: Ensure `CLIENT_URL` matches the exact frontend origin in `marathon-be/.env`.
