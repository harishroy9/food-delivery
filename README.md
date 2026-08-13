<div align="center">

# 🍔 FoodByte

### A Full-Stack Food Delivery Web Application

[![GitHub stars](https://img.shields.io/github/stars/harishroy9/food-delivery?style=social)](https://github.com/harishroy9/food-delivery/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/harishroy9/food-delivery?style=social)](https://github.com/harishroy9/food-delivery/network)
[![GitHub issues](https://img.shields.io/github/issues/harishroy9/food-delivery)](https://github.com/harishroy9/food-delivery/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**FoodByte** is a modern, feature-rich food delivery platform built with the **MERN Stack**. It brings together a beautiful customer storefront, a powerful admin dashboard, and a secure REST API backend — delivering a seamless end-to-end food ordering experience.

[View Demo](#) · [Report Bug](https://github.com/harishroy9/food-delivery/issues) · [Request Feature](https://github.com/harishroy9/food-delivery/issues)

</div>

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Running the App](#running-the-app)
- [API Overview](#api-overview)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 📖 About the Project

FoodByte is a complete food delivery solution inspired by modern food-tech platforms. The application allows customers to browse food items, add them to a cart, and securely place orders using Stripe payments. Restaurant admins can manage products and track live orders through a dedicated dashboard.

The project is organized as a **monorepo** with three separate applications:

| App | Description |
|-----|-------------|
| `frontend/` | Customer-facing React storefront |
| `admin/` | Admin dashboard for product & order management |
| `backend/` | Node.js + Express REST API server |

---

## ✨ Features

### 🛒 Customer Panel
- Browse food items with category filtering
- Add / remove items from cart
- Secure user registration & login (JWT)
- Stripe-powered online payments
- View and track past orders
- Responsive design for all screen sizes

### 🔧 Admin Panel
- Secure admin authentication
- Add new food items with image uploads
- View and delete existing products
- Manage and update live order statuses
- Role-based access control

### ⚙️ Backend API
- RESTful API architecture
- JWT authentication middleware
- Password hashing with Bcrypt
- File upload handling with Multer
- MongoDB data persistence with Mongoose
- Stripe webhook integration

---

## 🛠️ Tech Stack

### Frontend & Admin
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)

---

## 📁 Project Structure

```
food-delivery/
│
├── frontend/                   # Customer-facing React app
│   ├── public/
│   ├── src/
│   │   ├── assets/             # Images and static assets
│   │   ├── components/         # Reusable UI components
│   │   │   ├── Navbar/
│   │   │   ├── Footer/
│   │   │   ├── Header/
│   │   │   ├── FoodItem/
│   │   │   ├── FoodDisplay/
│   │   │   ├── ExploreMenu/
│   │   │   ├── AppDownload/
│   │   │   └── LoginPopup/
│   │   ├── context/            # React Context (global state)
│   │   └── pages/              # Page-level components
│   │       ├── Home/
│   │       ├── Cart/
│   │       ├── PlaceOrder/
│   │       ├── MyOrders/
│   │       └── Verify/
│   └── package.json
│
├── admin/                      # Admin dashboard React app
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar/
│   │   │   ├── Sidebar/
│   │   │   └── Login/
│   │   ├── context/
│   │   └── pages/
│   │       ├── Add/
│   │       ├── List/
│   │       └── Orders/
│   └── package.json
│
├── backend/                    # Node.js REST API
│   ├── config/                 # Database connection
│   ├── controllers/            # Route logic
│   ├── middleware/             # Auth middleware
│   ├── models/                 # Mongoose schemas
│   ├── routes/                 # API route definitions
│   ├── uploads/                # Multer file storage
│   ├── server.js
│   └── package.json
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) (v9 or higher)
- [MongoDB](https://www.mongodb.com/) (local or Atlas cloud)
- A [Stripe](https://stripe.com/) account for payment integration

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/harishroy9/food-delivery.git
cd food-delivery
```

2. **Install dependencies for all three apps**

```bash
# Install frontend dependencies
cd frontend
npm install

# Install admin dependencies
cd ../admin
npm install

# Install backend dependencies
cd ../backend
npm install
```

### Environment Variables

Create a `.env` file inside the `backend/` directory and add the following:

```env
# MongoDB connection string
MONGO_URL=your_mongodb_connection_url

# JWT secret key (use a strong random string)
JWT_SECRET=your_jwt_secret_key

# Bcrypt salt rounds
SALT=10

# Stripe secret key (from your Stripe dashboard)
STRIPE_SECRET_KEY=your_stripe_secret_key
```

> ⚠️ **Never commit your `.env` file to version control. Add it to `.gitignore`.**

### Configure Application URLs

Before running, update the API base URLs in the following files:

| File | Variable | Value |
|------|----------|-------|
| `frontend/src/context/StoreContext.jsx` | `const url` | Your backend URL |
| `admin/src/App.jsx` | `const url` | Your backend URL |
| `backend/controllers/orderController.js` | `const frontend_url` | Your frontend URL |

**For local development:**
```
Backend URL  → http://localhost:4000
Frontend URL → http://localhost:5173
Admin URL    → http://localhost:5174
```

### Running the App

Open **three separate terminals** and run:

```bash
# Terminal 1 — Start Backend
cd backend
npm run server

# Terminal 2 — Start Frontend
cd frontend
npm run dev

# Terminal 3 — Start Admin
cd admin
npm run dev
```

---

## 🔌 API Overview

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/user/register` | Register a new user |
| `POST` | `/api/user/login` | User login |
| `GET` | `/api/food/list` | Get all food items |
| `POST` | `/api/food/add` | Add a food item (admin) |
| `DELETE` | `/api/food/remove` | Delete a food item (admin) |
| `POST` | `/api/cart/add` | Add item to cart |
| `POST` | `/api/cart/remove` | Remove item from cart |
| `GET` | `/api/cart/get` | Get user's cart |
| `POST` | `/api/order/place` | Place a new order |
| `POST` | `/api/order/verify` | Verify Stripe payment |
| `GET` | `/api/order/userorders` | Get user's orders |
| `GET` | `/api/order/list` | Get all orders (admin) |
| `POST` | `/api/order/status` | Update order status (admin) |

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

1. **Fork** the repository by clicking the "Fork" button at the top of this page

2. **Clone** your forked repo locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/food-delivery.git
   cd food-delivery
   ```

3. **Create a new branch** for your feature or bug fix:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

4. **Make your changes** — write clean, well-documented code

5. **Commit your changes** with a descriptive message:
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```
   > Follow [Conventional Commits](https://www.conventionalcommits.org/) format where possible: `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`

6. **Push** to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Open a Pull Request** on GitHub and describe your changes clearly

### Contribution Guidelines

- ✅ Write clear and concise commit messages
- ✅ Keep pull requests focused on a single feature or fix
- ✅ Test your changes before submitting
- ✅ Update the README if you add new features or change setup steps
- ✅ Be respectful and constructive in code reviews
- ❌ Do not commit sensitive data (API keys, `.env` files)
- ❌ Avoid breaking existing functionality without discussion

### Reporting Issues

Found a bug or have a feature request? [Open an issue](https://github.com/harishroy9/food-delivery/issues) with:
- A clear title and description
- Steps to reproduce (for bugs)
- Expected vs actual behaviour
- Screenshots if applicable

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2025 harishroy9

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 📬 Contact

**harishroy9**

[![GitHub](https://img.shields.io/badge/GitHub-harishroy9-181717?style=for-the-badge&logo=github)](https://github.com/harishroy9)

📧 contact@foodbyte.com

---

<div align="center">

⭐ **If you found this project helpful, please give it a star!** ⭐

Made with ❤️ by [harishroy9](https://github.com/harishroy9)

</div>
