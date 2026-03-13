# E-Commerce App

A full-stack e-commerce web application with a Vue 3 frontend and a Node.js/Express backend deployed on AWS Lambda.

🔗 **Live Demo:** [e-commerce-app-frontend-rosy.vercel.app](https://e-commerce-app-frontend-rosy.vercel.app)

---

## Repositories

| Repo | Description |
|---|---|
| [e-commerce-app-frontend](https://github.com/karlits-exe/e-commerce-app-frontend) | Vue 3 + Vite frontend |
| [e-commerce-app-backend](https://github.com/karlits-exe/e-commerce-app-backend) | Node.js + Express REST API |

---

## Features

### Users
- User registration and login
- JWT-based authentication
- Update password
- Retrieve user details
- Promote user to admin (admin only)

### Products
- Create products (admin only)

### Cart
- View cart
- Add items to cart
- Update item quantities
- Remove individual items or clear the entire cart
- Per-item subtotals and cart total

### Orders
- Checkout / create an order (customers)
- View own order history (authenticated users)
- View all orders (admin only)

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vue 3, Vite, CSS |
| Backend | Node.js, Express |
| Auth | JWT |
| Deployment (Frontend) | Vercel |
| Deployment (Backend) | AWS Lambda |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18+
- npm

---

### Frontend Setup

```bash
git clone https://github.com/karlits-exe/e-commerce-app-frontend.git
cd e-commerce-app-frontend
npm install
```

Copy and configure environment variables:

```bash
cp .env .env.local
```

Start the dev server:

```bash
npm run dev
```

The app will be available at `http://localhost:5173`.

#### Frontend Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build |

---

### Backend Setup

```bash
git clone https://github.com/karlits-exe/e-commerce-app-backend.git
cd e-commerce-app-backend
npm install
```

Configure your environment variables (database connection string, JWT secret, etc.), then start the server:

```bash
node index.js
```

A Postman collection (`ECommerceApp.postman_collection.json`) is included in the repo for testing all API endpoints.

---

## Project Structure

### Frontend

```
e-commerce-app-frontend/
├── public/          # Static assets
├── src/
│   ├── assets/      # Images and styles
│   ├── components/  # Reusable Vue components
│   ├── views/       # Page-level components
│   └── main.js      # App entry point
├── index.html
└── vite.config.js
```

### Backend

```
e-commerce-app-backend/
├── controllers/     # Route handler logic
├── models/          # Data models
├── routes/          # API route definitions
├── auth.js          # JWT authentication middleware
├── index.js         # App entry point
└── lambda.js        # AWS Lambda handler
```

---

## Test Credentials

| Role | Email | Password |
|---|---|---|
| Admin | admin@mail.com | admin123 |
| Customer | jamesDoe@mail.com | sample123 |

---

## Deployment

- **Frontend** is deployed on [Vercel](https://vercel.com). Pushes to `main` trigger automatic deployments.
- **Backend** is deployed as an AWS Lambda function via `lambda.js`.

---
