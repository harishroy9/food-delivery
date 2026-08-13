# 🍔 FoodByte - Food Delivery Web App

FoodByte is a full-stack food delivery platform built with the **MERN Stack**. It provides a seamless online food ordering experience with a user-facing storefront, an admin management panel, and a robust REST API backend.

> **Author:** [harishroy9](https://github.com/harishroy9)
> **Repository:** [github.com/harishroy9/food-delivery](https://github.com/harishroy9/food-delivery)

---

## ✨ Features

### User Panel
- Browse food items by category
- Add to cart & place orders
- JWT-based Login / Signup & Logout
- Stripe Payment Integration
- Track My Orders
- Beautiful toast alerts

### Admin Panel
- Secure admin login
- Add, list & delete food products
- Manage and update orders
- Role-based access

### Backend
- RESTful APIs with Express.js
- MongoDB database with Mongoose
- Password hashing with Bcrypt
- Authenticated routes with JWT
- File uploads with Multer

---

## 🛠️ Tech Stack

| Layer     | Technology                          |
|-----------|-------------------------------------|
| Frontend  | React.js, React Router, Axios       |
| Admin     | React.js, React Router, Axios       |
| Backend   | Node.js, Express.js                 |
| Database  | MongoDB (Mongoose)                  |
| Auth      | JWT, Bcrypt                         |
| Payments  | Stripe                              |
| Uploads   | Multer                              |

---

## 🚀 Run Locally

### Clone the Repository

```bash
git clone https://github.com/harishroy9/food-delivery.git
cd food-delivery
```

### Install Dependencies

```bash
# Frontend
cd frontend && npm install

# Admin
cd ../admin && npm install

# Backend
cd ../backend && npm install
```

### Setup Environment Variables

Create a `.env` file inside the `backend/` folder:

```env
JWT_SECRET=your_jwt_secret_key
SALT=10
MONGO_URL=your_mongodb_connection_url
STRIPE_SECRET_KEY=your_stripe_secret_key
```

### Configure URLs

- **Admin** → `admin/src/App.jsx`: set `const url = "YOUR_BACKEND_URL"`
- **Frontend** → `frontend/src/context/StoreContext.jsx`: set `const url = "YOUR_BACKEND_URL"`
- **Backend** → `backend/controllers/orderController.js`: set `const frontend_url = "YOUR_FRONTEND_URL"`

### Start the Servers

```bash
# Backend (from /backend)
nodemon server.js

# Frontend (from /frontend)
npm run dev

# Admin (from /admin)
npm run dev
```

---

## 📁 Project Structure

```
food-delivery/
├── frontend/       # React user-facing app
├── admin/          # React admin panel
├── backend/        # Node.js + Express REST API
└── README.md
```

---

## 📬 Contact

- **GitHub:** [harishroy9](https://github.com/harishroy9)
- **Email:** contact@foodbyte.com

---

*© 2025 FoodByte — All Rights Reserved*
