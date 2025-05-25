# ART 'O' HOLIC – Art Selling Platform

Welcome to the official GitHub repository for **ART 'O' HOLIC**, a full-stack MERN web application designed to connect artists with art enthusiasts. This platform enables users to explore, customize, and purchase premium, handcrafted artwork — including portraits, seasonal pieces, and religious-themed art — directly from independent creators. Built with scalability, security, and reliability in mind, this application follows industry-standard practices for production-grade deployment.

## Features

- **Artwork Management**: Artists can upload and manage artwork using Cloudinary with optimized image processing.
- **Product Listings**: Browse product listings with filtering, sorting, and custom order options.
- **User Authentication**: Secure user registration and login with JWT and OAuth 2.0 support.
- **Payments**: Secure payment processing via Stripe or Razorpay with PCI compliance.
- **Order Management**: Real-time order tracking and a comprehensive administrative dashboard.
- **Responsive Design**: Accessible frontend with support for dark/light modes and WCAG compliance.
- **Scalability**: Horizontal scaling with load balancing and caching for high traffic.
- **Security**: Robust protections against common vulnerabilities (e.g., XSS, CSRF, SQL injection).
- **Monitoring**: Real-time monitoring and logging for performance and error tracking.

## Tech Stack

### Frontend
- **React (Vite)**: Fast, component-based UI with hot module replacement.
- **Tailwind CSS**: Utility-first CSS for responsive and maintainable styling.
- **React Router**: Client-side routing for seamless navigation.
- **Axios**: HTTP client for API communication with retry mechanisms.
- **React Query**: Data fetching and state management for optimized API calls.

### Backend
- **Node.js with Express**: RESTful API with middleware for security and performance.
- **MongoDB Atlas with Mongoose**: Scalable NoSQL database with schema validation.
- **JSON Web Token (JWT)**: Secure authentication with refresh tokens.
- **Rate Limiting**: Prevents abuse using express-rate-limit.
- **Helmet**: Secures HTTP headers to mitigate common attacks.
- **Winston**: Centralized logging for debugging and monitoring.

### Integrations & Deployment
- **Cloudinary**: Image hosting with CDN for fast delivery.
- **Stripe / Razorpay**: Secure payment gateways with webhook support.
- **GitHub Actions**: CI/CD pipelines for automated testing and deployment.
- **Vercel**: Frontend hosting with automatic scaling and domain management.
- **Render**: Backend hosting with managed scaling and health checks.
- **Sentry**: Real-time error tracking and performance monitoring.
- **New Relic**: Application performance monitoring (APM) for bottlenecks.
- **Redis**: Caching layer for improved API response times.
- **Cloudflare**: DDoS protection, WAF, and CDN for global performance.

## Production Environment

To ensure a bug-free and attack-resistant platform, ART 'O' HOLIC incorporates the following production-grade practices:

### Security
- **Authentication**: JWT with refresh tokens, OAuth 2.0 for third-party logins (Google, GitHub).
- **Authorization**: Role-based access control (RBAC) for users, artists, and admins.
- **Input Validation**: Sanitization and validation using Joi or express-validator to prevent injection attacks.
- **HTTPS**: Enforced TLS/SSL for secure data transmission.
- **CORS**: Strict CORS policies to prevent unauthorized API access.
- **CSRF Protection**: CSRF tokens for all state-changing requests.
- **Rate Limiting**: Prevents brute-force and DDoS attacks.
- **WAF**: Cloudflare Web Application Firewall to filter malicious traffic.
- **Secrets Management**: Environment variables stored securely in Vercel/Render and encrypted at rest.
- **Dependency Scanning**: Dependabot and Snyk for vulnerability detection in dependencies.

### Scalability
- **Load Balancing**: Managed by Vercel (frontend) and Render (backend) for distributing traffic.
- **Caching**: Redis for caching frequent API responses and session data.
- **Database Optimization**: MongoDB Atlas with indexes and sharding for high throughput.
- **Horizontal Scaling**: Auto-scaling backend instances based on traffic demand.
- **CDN**: Cloudinary and Cloudflare for global content delivery.

### Monitoring & Logging
- **Sentry**: Real-time error tracking with stack traces and user context.
- **New Relic**: Monitors API performance, database queries, and server health.
- **Winston**: Structured logging with rotation and centralized storage.
- **Health Checks**: Endpoint for monitoring service availability (`/health`).
- **Uptime Monitoring**: Integrated with Render and Vercel for 99.9% uptime.

### Testing
- **Unit Tests**: Jest and React Testing Library for frontend components; Mocha/Chai for backend.
- **Integration Tests**: Test API endpoints with Supertest and mocked MongoDB.
- **End-to-End Tests**: Cypress for simulating user flows (e.g., checkout, artwork upload).
- **Security Testing**: OWASP ZAP for automated vulnerability scanning.
- **Load Testing**: Artillery for simulating high traffic and ensuring scalability.

### CI/CD
- **GitHub Actions**: Automated workflows for linting, testing, and deployment.
- **Zero-Downtime Deployment**: Blue-green deployment strategy on Render.
- **Environment Separation**: Distinct development, staging, and production environments.
- **Rollback**: Automated rollback on deployment failures via GitHub Actions.

## Folder Structure

```
art-o-holic/
├── client/                     # React frontend (hosted on Vercel)
│   ├── public/                # Static assets
│   ├── src/
│   │   ├── components/        # Reusable React components
│   │   ├── pages/             # Page-level components
│   │   ├── hooks/             # Custom React hooks
│   │   ├── utils/             # Utility functions (e.g., API helpers)
│   │   └── assets/            # Local images, fonts, etc.
│   ├── .env                   # Frontend env vars (e.g., VITE_API_URL)
│   ├── vite.config.js         # Vite configuration
│   └── package.json
│
├── server/                     # Express backend (hosted on Render)
│   ├── controllers/           # Request handlers
│   ├── models/                # Mongoose schemas
│   ├── routes/                # API routes
│   ├── middleware/            # Custom middleware (auth, error handling)
│   ├── utils/                 # Utility functions (e.g., logging, error handling)
│   ├── config/                # Configuration files (e.g., DB, Cloudinary)
│   ├── tests/                 # Unit and integration tests
│   ├── .env                   # Backend env vars (DB URI, API keys)
│   └── package.json
│
├── .github/                    # GitHub workflows for CI/CD
│   └── workflows/
│       ├── frontend.yml       # Frontend lint, test, and deploy
│       ├── backend.yml        # Backend lint, test, and deploy
│       └── security.yml       # Dependency and code scanning
│
├── README.md
└── .gitignore
```

## Getting Started

### Prerequisites
- Node.js (v18+)
- MongoDB Atlas account
- Cloudinary account
- Stripe or Razorpay account
- Vercel and Render accounts
- Redis instance (optional for caching)

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/username/art-o-holic.git
   cd art-o-holic
   ```

2. **Install dependencies**:
   ```bash
   cd client && npm install
   cd ../server && npm install
   ```

3. **Set up environment variables**:
   - Create `.env` files in `client/` and `server/` based on `.env.example`.
   - Example `.env` for `client`:
     ```
     VITE_API_URL=https://api.artoholic.com
     VITE_CLOUDINARY_CLOUD_NAME=your_cloud_name
     VITE_STRIPE_PUBLIC_KEY=your_stripe_key
     ```
   - Example `.env` for `server`:
     ```
     PORT=5000
     MONGO_URI=mongodb+srv://user:pass@cluster0.mongodb.net/artoholic
     JWT_SECRET=your_jwt_secret
     CLOUDINARY_URL=cloudinary://api_key:api_secret@cloud_name
     STRIPE_SECRET_KEY=your_stripe_secret
     REDIS_URL=redis://your_redis_instance
     ```

4. **Run locally**:
   - Frontend: `cd client && npm run dev`
   - Backend: `cd server && npm run dev`

### Deployment
1. **Frontend (Vercel)**:
   - Push `client/` to a GitHub repository.
   - Connect to Vercel, set environment variables, and deploy.
2. **Backend (Render)**:
   - Push `server/` to a GitHub repository.
   - Connect to Render, configure environment variables, and deploy with health checks.
3. **CI/CD**:
   - GitHub Actions workflows in `.github/workflows/` handle linting, testing, and deployment.
   - Ensure secrets (e.g., `VERCEL_TOKEN`, `RENDER_API_KEY`) are added to GitHub repository settings.

## Security Best Practices
- **Sanitize Inputs**: All user inputs are validated and sanitized to prevent XSS and injection attacks.
- **Secure APIs**: APIs are protected with JWT, rate limiting, and CORS.
- **Environment Variables**: Sensitive data (e.g., API keys) is stored securely and never hardcoded.
- **Regular Audits**: Automated security scans with OWASP ZAP and Snyk.
- **HTTPS Everywhere**: Enforced via Vercel and Render configurations.
- **Backup & Recovery**: MongoDB Atlas automated backups with point-in-time recovery.

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/xyz`).
3. Commit changes (`git commit -m "Add feature xyz"`).
4. Push to the branch (`git push origin feature/xyz`).
5. Open a pull request with detailed descriptions and test results.

## Testing
Run tests to ensure code quality:
```bash
# Frontend tests
cd client && npm run test

# Backend tests
cd server && npm run test

# End-to-end tests
cd client && npm run cypress
```

## Monitoring
- **Sentry**: Configure with your DSN in `.env` for error tracking.
- **New Relic**: Add your license key in `.env` for APM.
- **Logs**: Access centralized logs via Render or a logging service like Loggly.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For inquiries, reach out to the ART 'O' HOLIC team at [support@artoholic.com](mailto:support@artoholic.com).
