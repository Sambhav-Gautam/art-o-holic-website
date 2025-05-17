# 🎨 ART 'O' HOLIC – Art Selling Platform

Welcome to the official GitHub repository for **ART 'O' HOLIC**, a full-stack MERN web application that enables users to explore, order, and pay for custom and premium artworks. Whether it's portraits, seasonal art, or religious themes – ART 'O' HOLIC delivers handcrafted pieces straight from artists to customers.

## 🚀 Features

- 🖼 Upload & manage artwork with Cloudinary
- 🛒 Browse product listings and custom offerings
- 👤 User registration & login system
- 💳 Secure payments via Stripe or Razorpay
- 📦 Order tracking and admin dashboard
- 🌐 Responsive, accessible frontend with dark/light mode

## 🧰 Tech Stack

**Frontend**
- React (Vite)
- Tailwind CSS
- React Router
- Axios

**Backend**
- Node.js + Express
- MongoDB Atlas (Mongoose)
- JWT Authentication

**Other Integrations**
- Cloudinary (Image hosting)
- Stripe / Razorpay (Payments)
- GitHub Actions (CI/CD)
- Vercel / Netlify (Frontend Hosting)
- Render / Railway (Backend Hosting)

## 📁 Folder Structure
art-o-holic/
├── client/                 # React frontend (hosted on Vercel/Netlify)
│   ├── public/
│   ├── src/
│   ├── .env               # FRONTEND env variables (e.g., REACT_APP_API_URL)
│   └── package.json
│
├── server/                 # Express backend (hosted on Render/Railway/Heroku)
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── config/
│   ├── .env               # BACKEND env variables (DB URI, Cloudinary keys, etc.)
│   └── package.json
│
├── .github/               # GitHub workflows for CI/CD
│   └── workflows/
│       ├── frontend.yml   # Vercel CI/CD or Netlify build test
│       └── backend.yml    # Render or Railway CI/CD triggers
│
├── README.md
└── .gitignore

