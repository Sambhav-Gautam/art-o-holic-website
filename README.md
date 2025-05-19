# ART 'O' HOLIC – Art Selling Platform

Welcome to the official GitHub repository for **ART 'O' HOLIC**, a full-stack MERN web application that connects artists with art enthusiasts. This platform allows users to explore, customize, and purchase premium, handcrafted artwork — including portraits, seasonal pieces, and religious-themed art — directly from independent creators.

## Features

* Upload and manage artwork using Cloudinary
* Browse product listings and custom order options
* User registration and authentication
* Secure payment integration via Stripe or Razorpay
* Order tracking and administrative dashboard
* Responsive, accessible frontend with support for dark and light modes

## Tech Stack

**Frontend**

* React (Vite)
* Tailwind CSS
* React Router
* Axios

**Backend**

* Node.js with Express
* MongoDB Atlas with Mongoose
* JSON Web Token (JWT) authentication

**Integrations & Deployment**

* Cloudinary (Image hosting)
* Stripe / Razorpay (Payments)
* GitHub Actions (CI/CD)
* Vercel or Netlify (Frontend Hosting)
* Render or Railway (Backend Hosting)

## Folder Structure

```
art-o-holic/
├── client/                 # React frontend (hosted on Vercel or Netlify)
│   ├── public/
│   ├── src/
│   ├── .env                # Frontend environment variables (e.g., REACT_APP_API_URL)
│   └── package.json
│
├── server/                 # Express backend (hosted on Render or Railway)
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── config/
│   ├── .env                # Backend environment variables (DB URI, Cloudinary keys, etc.)
│   └── package.json
│
├── .github/                # GitHub workflows for CI/CD
│   └── workflows/
│       ├── frontend.yml    # Frontend build and deployment
│       └── backend.yml     # Backend deployment and testing
│
├── README.md
└── .gitignore
```
