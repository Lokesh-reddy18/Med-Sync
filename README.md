# MedSync

A full‑stack healthcare appointment platform composed of three components:
- `frontend`: Patient-facing web app
- `admin`: Administrative dashboard
- `backend`: REST API server

## 🔗 Live Links

- Frontend: `https://med-sync-client.vercel.app/`
- Admin: `https://med-sync-admin.vercel.app/`
- API: `https://medsync-server.onrender.com`

## 🏗️ Repository Structure

```
summerintern/
├─ frontend/        # Patient-facing React app (Vite + Tailwind)
├─ admin/           # Admin dashboard (Vite + Tailwind)
└─ backend/         # Node/Express API server
```

### Subproject Highlights
- `frontend`
  - Auth, doctor discovery, appointment booking, Stripe payments, profiles
  - Tech: React, Vite, Tailwind CSS, Axios, React Router, React Toastify, Stripe
- `admin`
  - Admin auth, doctors/users management, appointments oversight, payments, analytics
  - Tech: React, Vite, Tailwind CSS, Axios, React Router, React Toastify
- `backend`
  - REST API, JWT auth, doctors/users, appointments, Stripe, Cloudinary
  - Tech: Node, Express, MongoDB, Mongoose, JWT, Bcrypt, Stripe, Cloudinary, Multer

## ✅ Prerequisites
- Node.js 18+
- npm 9+
- A MongoDB database
- Stripe account and secret key
- Cloudinary account and API keys

## ⚙️ Environment Variables
Create a `.env` file in each subproject with the following keys.

### frontend/.env
```
VITE_BACKEND_URL=https://medsync-server.onrender.com
```

### admin/.env
```
VITE_BACKEND_URL=https://medsync-server.onrender.com
```

### backend/.env
```
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

## 🚀 Quick Start (Local Development)
Open three terminals from the repo root and run each app.

### 1) Backend API
```
cd backend
npm install
npm run dev
```
- Default server: typically `http://localhost:4000` (check `backend/server.js`)

### 2) Frontend (Patient App)
```
cd frontend
npm install
npm run dev
```
- Vite dev server prints the local URL (commonly `http://localhost:5173`)

### 3) Admin Dashboard
```
cd admin
npm install
npm run dev
```
- Vite dev server prints the local URL (commonly `http://localhost:5174`)

Ensure `VITE_BACKEND_URL` in both frontend and admin points to your running backend URL during development.

## 📦 Production Builds
Generate optimized builds for frontend and admin.

```
cd frontend && npm run build
cd ../admin && npm run build
```

Deploy the `backend` to your server/platform (e.g., Render), configure env vars, and serve the built `frontend`/`admin` (e.g., on Vercel/Netlify) with `VITE_BACKEND_URL` set to the deployed API.

## 🔌 API Overview (Backend)
High-level routes (representative; consult code for full details):
- Auth: `POST /api/user/register`, `POST /api/user/login`, `POST /api/doctor/register`, `POST /api/doctor/login`
- Users: `GET /api/user/profile`, `PUT /api/user/profile`, `GET /api/user/appointments`
- Doctors: `GET /api/doctor/list`, `GET /api/doctor/profile`, `PUT /api/doctor/profile`

## 🔐 Access Notes
- Admin panel access requires admin credentials provisioned by the system administrator.

## 🧪 Scripts Reference
Each subproject exposes common scripts:
- `npm install` – install dependencies
- `npm run dev` – start development server
- `npm run build` – production build (frontend/admin)

