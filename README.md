# 🛍️ ShopStream

A full-stack MERN e-commerce platform with buyer and seller experiences — product catalog with variants, cart & wishlist, Razorpay checkout, order management, seller analytics, reviews, and Google OAuth login.

**🔗 Live Demo:**[ [https://shopstream-js68.onrender.com](https://shopstream-js68.onrender.com)]

---

## ✨ Features

### Buyer
- Browse products with category/subcategory filters
- Product variants (size, color, etc.)
- Cart & wishlist management
- Product reviews & ratings
- Razorpay-powered checkout
- Order history & order detail tracking
- Restock waitlist notifications for out-of-stock items
- "Frequently bought together" and "Complete the look" recommendations
- Email/password auth, Google OAuth, and password reset flow

### Seller
- Create, update, and delete product listings with image uploads (ImageKit)
- Manage product variants
- View and reply to customer reviews
- Order management dashboard
- Seller analytics dashboard

---

## 🧱 Tech Stack

**Frontend**
- React 19 + Vite (Rolldown)
- Redux Toolkit
- React Router v7
- Tailwind CSS 4
- Framer Motion, Lenis (smooth scroll)
- Axios, React Hot Toast / Sonner
- Razorpay React SDK

**Backend**
- Node.js + Express 5
- MongoDB + Mongoose
- Redis (ioredis)
- JWT authentication + Passport (Google OAuth 2.0)
- Multer + ImageKit (image storage)
- Razorpay (payments)
- Nodemailer (transactional email)
- Helmet, CORS, express-rate-limit, express-validator (security & validation)

---

## 📂 Project Structure

```
ShopStream/
├── Backend/
│   ├── server.js
│   └── src/
│       ├── config/        # DB, env, and third-party config
│       ├── controllers/    # Route handlers
│       ├── routes/         # Express routers (auth, product, cart, wishlist, order)
│       ├── models/         # Mongoose schemas
│       ├── daos/           # Data access layer
│       ├── services/       # Business logic
│       ├── validators/     # express-validator schemas
│       ├── Middleware/     # Auth & seller middleware
│       └── utils/
└── frontend/
    └── src/
        ├── App/
        ├── components/
        ├── context/
        └── features/
            ├── auth/
            ├── cart/
            ├── legal/
            ├── products/
            └── wishlist/
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+ recommended)
- MongoDB instance (local or Atlas)
- Redis instance
- Razorpay account (test keys)
- Google OAuth credentials
- ImageKit account

### 1. Clone the repo
```bash
git clone https://github.com/St0rmsh/ShopStream.git
cd ShopStream
```

### 2. Backend setup
```bash
cd Backend
npm install
```

Create a `.env` file in `Backend/` with:
```env
PORT=8080
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_SECRET=your_google_client_secret
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
REDIS_HOST=your_redis_host
REDIS_PORT=your_redis_port
REDIS_PASSWORD=your_redis_password
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
```

Run the backend:
```bash
npm run dev
```

### 3. Frontend setup
```bash
cd ../frontend
npm install
npm run dev
```

The frontend runs on Vite's default dev server (typically `http://localhost:5173`) and the backend defaults to the port set in `.env`.

---

## 📡 API Overview

| Resource  | Base Route         | Description                                  |
|-----------|---------------------|-----------------------------------------------|
| Auth      | `/api/auth`         | Register, login, Google OAuth, password reset |
| Products  | `/api/product`      | CRUD, variants, reviews, categories           |
| Cart      | `/api/cart`         | Add/update/remove cart items                  |
| Wishlist  | `/api/wishlist`     | Toggle & fetch wishlist                       |
| Orders    | `/api/order`        | Checkout, payment, order history, seller orders, analytics |

---

## 🌐 Deployment

The app is deployed and live at **[streamline-chez.onrender.com](https://streamline-chez.onrender.com)**, hosted on [Render](https://render.com).

---

## 📄 License

This project currently has no explicit license. Contact the repository owner ([St0rmsh](https://github.com/St0rmsh)) for usage permissions.
