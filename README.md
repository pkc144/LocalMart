
````markdown
# 🛒 LOCALMART (MERN Ecommerce App)

A Full-Stack Ecommerce application built using **MongoDB, Express, React (TypeScript), Node.js** with **Stripe payment integration**, **Firebase authentication**, and **Redis caching**.

---

## 🚀 Backend Setup

### Install Dependencies
```bash
cd backend
npm install
npm run build   # or npm run dev for development
````

### Env Variables

Create a `.env` file in `backend/` with:

```
PORT=4000
MONGO_URI=mongodb://localhost:27017/localmart
STRIPE_KEY=your_stripe_secret_key
PRODUCT_PER_PAGE=8
REDIS_URL=redis://localhost:6379
```

---

## 💻 Frontend Setup

### Install Dependencies

```bash
cd frontend
npm install
npm run dev       # start development server
npm run preview   # preview production build
```

### Env Variables

Create a `.env` file in `frontend/` with:

```
VITE_FIREBASE_KEY=your_firebase_key
VITE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_PROJECT_ID=your_firebase_project_id
VITE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_MESSAGING_SENDER_ID=your_firebase_sender_id
VITE_APP_ID=your_firebase_app_id
VITE_SERVER=http://localhost:4000
VITE_STRIPE_KEY=your_stripe_publishable_key
```

---

## 🎨 Styling

* The frontend uses **SCSS** for modular and scalable styling.
* Global variables and mixins are placed under `/src/styles/`.
* Each component has its own `.scss` file for encapsulated styling.

---

## 📌 API Routes

### 🔑 Auth & User

* `POST /api/v1/user/new` → Register new user
* `POST /api/v1/user/login` → Login user
* `GET /api/v1/user/me` → Get logged-in user
* `GET /api/v1/user/all` → Get all users (**Admin only**)
* `GET /api/v1/user/:id` → Get user by ID
* `DELETE /api/v1/user/:id` → Delete user (**Admin only**)

---

### 🛍️ Products

* `GET /api/v1/product` → Get all products
* `GET /api/v1/product/:id` → Get single product
* `POST /api/v1/product/new` → Create product (**Admin only**)
* `PUT /api/v1/product/:id` → Update product (**Admin only**)
* `DELETE /api/v1/product/:id` → Delete product (**Admin only**)

---

### 📦 Orders

* `POST /api/v1/order/new` → Place new order
* `GET /api/v1/order/:id` → Get order details
* `GET /api/v1/order/me` → Get my orders
* `GET /api/v1/admin/orders` → Get all orders (**Admin only**)
* `PUT /api/v1/admin/order/:id` → Update order status (**Admin only**)
* `DELETE /api/v1/admin/order/:id` → Delete order (**Admin only**)

---

### 💳 Payments & Coupons

* `POST /api/v1/payment/create` → Create Stripe payment intent
* `POST /api/v1/payment/coupon/new` → Create new coupon (**Admin only**)
* `GET /api/v1/payment/discount` → Apply discount
* `GET /api/v1/payment/coupon/all` → Get all coupons (**Admin only**)
* `DELETE /api/v1/payment/coupon/:id` → Delete coupon (**Admin only**)

---

### 📊 Admin Dashboard

* `GET /api/v1/dashboard/stats` → Get dashboard stats (**Admin only**)
* `GET /api/v1/dashboard/pie` → Get pie chart data (**Admin only**)
* `GET /api/v1/dashboard/bar` → Get bar chart data (**Admin only**)
* `GET /api/v1/dashboard/line` → Get line chart data (**Admin only**)

---

## ⚡ Redis Caching

* Redis is used for caching frequently accessed data (products, stats, etc.).
* Default connection: `redis://localhost:6379`
* Configurable via `REDIS_URL` in `.env`.

---

## 🧪 Example Requests

### Register User

```json
POST /api/v1/user/new
{
  "name": "Alice",
  "email": "alice@example.com",
  "password": "password123"
}
```

### Create Product (Admin)

```json
POST /api/v1/product/new
{
  "name": "Laptop",
  "price": 900,
  "stock": 10,
  "category": "Electronics",
  "description": "Powerful laptop with 16GB RAM"
}
```

---

## ⚡ Features

* User Authentication (Firebase + JWT)
* Role-based access (Admin / User)
* Product management (CRUD)
* Cart & Orders
* Stripe Payment Integration
* Redis Caching
* SCSS styling
* Admin Dashboard with Stats (Charts, Orders, Users, Coupons)

---

## 🛠️ Tech Stack

* **Frontend:** React (TypeScript), SCSS
* **Backend:** Node.js, Express.js
* **Database:** MongoDB
* **Cache:** Redis
* **Auth:** Firebase Authentication
* **Payments:** Stripe

```


