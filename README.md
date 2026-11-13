# STRIDEFORGE Events — Marathon Event Management System

[![Repository](https://img.shields.io/badge/GitHub-JeevananthanV%2Fmarathon__event-blue?logo=github)](https://github.com/JeevananthanV/marathon_event)
[![Frontend](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB?logo=react&logoColor=white)](http://localhost:5173)
[![Backend](https://img.shields.io/badge/Backend-Node.js%20%2B%20Express-339933?logo=nodedotjs&logoColor=white)](http://localhost:5000)
[![Database](https://img.shields.io/badge/Database-MongoDB%20Atlas-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/atlas)

A monorepo for India's premium marathon event series. Built with a React frontend and a Node.js + Express + MongoDB backend.

## 🔗 Repository Links

| Detail | Link |
|---|---|
| **GitHub Repository** | [https://github.com/JeevananthanV/marathon_event](https://github.com/JeevananthanV/marathon_event) |
| **Author** | [Jeevananthan V](https://github.com/JeevananthanV) |
| **Frontend Dev Server** | `http://localhost:5173` |
| **Backend API** | `http://localhost:5000/api` |

## Repository Structure

```
Marathon_Event/
├── marathon-fe/          # React + Vite frontend
│   ├── src/              # Application source
│   ├── public/           # Static assets
│   └── README.md         # Frontend documentation
└── marathon-be/          # Node.js + Express backend
    ├── src/
    │   ├── config/       # Database configuration
    │   ├── controllers/  # Route handlers
    │   ├── middleware/    # Express middleware
    │   ├── models/       # Mongoose models
    │   ├── routes/       # API route definitions
    │   ├── utils/        # Helper functions
    │   └── validations/  # Request validation rules
    └── package.json
```

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React, Vite, Tailwind CSS, GSAP |
| **Backend** | Node.js, Express, MongoDB Atlas, Mongoose |

## Setup Instructions

### Prerequisites

- Node.js >= 18
- npm
- MongoDB Atlas connection string (for backend)

### Clone

```bash
git clone https://github.com/JeevananthanV/marathon_event.git
cd marathon_event
```

### Frontend

```bash
cd marathon-fe
npm install
npm run dev
```

The frontend dev server starts at `http://localhost:5173`.

Create a `.env` file in `marathon-fe/`:

```env
VITE_API_URL=http://localhost:5000/api
```

### Backend

```bash
cd marathon-be
npm install
```

Create a `.env` file in `marathon-be/`:

```env
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/marathon?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_here
PORT=5000
```

```bash
npm run dev
```

The backend starts at `http://localhost:5000`.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive a JWT |
| GET | `/api/health` | Health check |

## Environment Variables

| Variable | Description |
|---|---|
| `MONGODB_URI` | MongoDB Atlas connection string |
| `JWT_SECRET` | Secret key for JWT signing |
| `PORT` | Server port (default: 5000) |

## Author

**Jeevananthan V** — [@JeevananthanV](https://github.com/JeevananthanV)

## License

MIT
