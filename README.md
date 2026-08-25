# 🍔 FoodAI – AI Powered Food Ordering Platform

**FoodAI** is a full-stack **MERN-based food ordering platform** that combines online food ordering with AI-powered food assistance and review analysis.

The platform allows users to discover restaurants and food items, manage their cart, apply coupons, place orders, make payments, and receive AI-based food recommendations. It also provides backend APIs for authentication, restaurant management, food management, orders, payments, coupons, and AI services.

---

## ✨ Features

### 👤 User Features

* 🔐 User Registration & Login
* 🔑 Secure JWT Authentication
* 👤 User Profile Management
* 🔄 Update User Profile
* 🔒 Role-based Authorization
* 🔑 Password Reset / Recovery
* 📧 Email Support for Authentication
* 🍽️ Browse Restaurants
* 🍕 Browse Food Items
* 🔎 Search Food
* 🗂️ Menu & Category Management
* 🛒 Add Food Items to Cart
* ➕ Increase / Decrease Quantity
* ❌ Remove Items from Cart
* 📦 Place Food Orders
* 📋 View Order History
* 🔍 View Order Details
* 💳 Payment Integration
* 🎟️ Apply Coupons
* 🏠 Manage Delivery Information

---

## 🤖 AI Features

FoodAI includes a dedicated AI module for improving the food discovery experience.

### AI Food Assistant

The application provides AI-powered assistance for food-related queries and recommendations.

### 🍽️ Food Recommendations

AI services can help users discover suitable food based on their requirements and preferences.

### ⭐ AI Review Analysis

The project also includes an AI-based review analysis service:

```text
aiReviewAnalyzer.js
```

This service is designed to process and analyze food/customer reviews using AI.

### AI Backend Architecture

```text
Frontend
   │
   ▼
AI API Route
   │
   ▼
AI Controller
   │
   ▼
AI Service
   │
   ▼
AI Processing / Recommendation
```

---

# 🏪 Restaurant Management

The backend contains a dedicated restaurant management module.

### Restaurant functionality includes:

* Create Restaurant
* Get Restaurants
* Restaurant Details
* Restaurant Count
* Restaurant-based Food/Menu Management

Relevant backend files:

```text
controllers/restaurantController.js
routes/restaurant.js
routes/restaurant_count.js
models/restaurant.js
```

---

# 🍕 Food & Menu Management

FoodAI provides dedicated APIs and models for managing food items and menus.

### Food functionality

* Add Food Item
* Get Food Items
* Update Food Item
* Delete Food Item
* Food Search
* Menu Management
* Restaurant-based Food Management

Backend structure:

```text
controllers/
├── foodItemController.js
└── menuController.js

models/
├── foodItem.js
└── menu.js

routes/
├── foodItem.js
└── menu.js
```

---

# 🛒 Cart System

The cart module allows users to manage their selected food items before placing an order.

### Cart Features

* Add item to cart
* Update quantity
* Remove item
* Calculate cart information
* Manage user-specific cart

```text
cartController.js
cartModel.js
cart.js
```

---

# 📦 Order Management

Users can place and manage their food orders.

### Order Features

* Create Order
* View Orders
* View Order Details
* User-specific Orders
* Order Management
* Order Status Handling

Backend:

```text
controllers/orderController.js
models/order.js
routes/order.js
```

---

# 💳 Payment System

FoodAI includes a dedicated payment module for processing food orders.

```text
controllers/paymentController.js
routes/payment.js
```

The payment system is connected with the order workflow so that users can complete their food orders through the application.

---

# 🎟️ Coupon System

The application includes a coupon management system.

### Coupon Features

* Create Coupons
* Apply Coupons
* Validate Coupons
* Manage Coupon Data

Backend:

```text
controllers/couponController.js
models/couponModel.js
routes/couponRoutes.js
```

---

# 🔐 Authentication & Authorization

FoodAI implements secure authentication and role-based authorization.

### Security Features

* JWT Authentication
* Protected Routes
* Password Hashing
* Role-based Access Control
* Authentication Middleware
* Error Handling
* Secure Environment Variables

Authorization middleware:

```text
middlewares/authorizeRoles.js
```

Authentication-related functionality:

```text
controllers/authController.js
routes/auth.js
models/user.js
utils/sendToken.js
utils/email.js
```

---

# ☁️ Cloudinary Integration

FoodAI uses **Cloudinary** for handling and storing food/restaurant images.

Configuration:

```text
backend/config/cloudinary.js
```

This allows the application to efficiently manage uploaded images without storing large media files directly inside the database.

---

# 📧 Email & Password Recovery

The backend includes email utilities and a Pug template for password reset functionality.

```text
utils/email.js
view/passwordReset.pug
```

This can be used for sending authentication-related emails such as password recovery.

---

# 🛠️ Tech Stack

## Frontend

| Technology    | Purpose                  |
| ------------- | ------------------------ |
| React.js      | Frontend UI              |
| Vite          | Development & Build Tool |
| Redux Toolkit | Global State Management  |
| React Router  | Client-side Routing      |
| Axios         | API Requests             |
| JavaScript    | Application Logic        |
| CSS           | Styling                  |

---

## Backend

| Technology | Purpose                     |
| ---------- | --------------------------- |
| Node.js    | Server Runtime              |
| Express.js | Backend Framework           |
| MongoDB    | Database                    |
| Mongoose   | MongoDB ODM                 |
| JWT        | Authentication              |
| bcrypt     | Password Security           |
| Nodemailer | Email Services              |
| Pug        | Password Reset Template     |
| Cloudinary | Image Management            |
| REST API   | Client-Server Communication |

---

## AI

* AI Service Integration
* AI Food Recommendation
* AI Food Assistance
* AI Review Analysis

---

# 📁 Project Structure

```text
FoodAiProject/
│
├── backend/
│   │
│   ├── config/
│   │   ├── cloudinary.js
│   │   ├── config.env
│   │   └── database.js
│   │
│   ├── controllers/
│   │   ├── ai.controller.js
│   │   ├── authController.js
│   │   ├── cartController.js
│   │   ├── couponController.js
│   │   ├── foodItemController.js
│   │   ├── menuController.js
│   │   ├── orderController.js
│   │   ├── paymentController.js
│   │   └── restaurantController.js
│   │
│   ├── middlewares/
│   │   ├── authorizeRoles.js
│   │   ├── catchAsyncErrors.js
│   │   └── errors.js
│   │
│   ├── models/
│   │   ├── cartModel.js
│   │   ├── couponModel.js
│   │   ├── foodItem.js
│   │   ├── menu.js
│   │   ├── order.js
│   │   ├── restaurant.js
│   │   └── user.js
│   │
│   ├── routes/
│   │   ├── ai.routes.js
│   │   ├── auth.js
│   │   ├── cart.js
│   │   ├── couponRoutes.js
│   │   ├── foodItem.js
│   │   ├── menu.js
│   │   ├── order.js
│   │   ├── payment.js
│   │   ├── restaurant.js
│   │   └── restaurant_count.js
│   │
│   ├── services/
│   │   ├── ai.service.js
│   │   └── aiReviewAnalyzer.js
│   │
│   ├── utils/
│   │   ├── apiFeatures.js
│   │   ├── email.js
│   │   ├── errorHandler.js
│   │   ├── seeder.js
│   │   └── sendToken.js
│   │
│   ├── view/
│   │   └── passwordReset.pug
│   │
│   ├── app.js
│   ├── server.js
│   └── package.json
│
└── frontend/
    │
    ├── public/
    │   └── images/
    │
    ├── src/
    │   │
    │   ├── assets/
    │   │
    │   ├── components/
    │   │   ├── cart/
    │   │   ├── layout/
    │   │   ├── order/
    │   │   ├── user/
    │   │   ├── CountRestaurant.jsx
    │   │   ├── Fooditem.jsx
    │   │   ├── Home.jsx
    │   │   ├── Menu.jsx
    │   │   ├── Restaurant.jsx
    │   │   └── Search.jsx
    │   │
    │   ├── redux/
    │   │   ├── actions/
    │   │   ├── slices/
    │   │   └── store.js
    │   │
    │   ├── utils/
    │   │   └── api.js
    │   │
    │   ├── App.jsx
    │   ├── App.css
    │   ├── index.css
    │   └── main.jsx
    │
    ├── index.html
    ├── vite.config.js
    └── package.json
```

---

# 🔄 Application Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React + Vite      │
                    │      Frontend       │
                    └──────────┬──────────┘
                               │
                         Axios / REST API
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Express.js       │
                    │       Backend       │
                    └──────────┬──────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
          ▼                    ▼                    ▼
   Authentication          Food/Menu            AI Services
          │                    │                    │
          ▼                    ▼                    ▼
       Orders              Restaurant         AI Recommendation
          │                    │               Review Analysis
          ▼                    ▼
       Payment              Coupons
          │                    │
          └──────────┬─────────┘
                     ▼
              ┌──────────────┐
              │   MongoDB    │
              └──────────────┘
```

---

# ⚙️ Installation & Setup

## 1. Clone Repository

```bash
git clone https://github.com/YOUR-USERNAME/FoodAiProject.git
cd FoodAiProject
```

---

## 2. Backend Setup

```bash
cd backend
npm install
```

Create your environment configuration according to your local setup.

Example:

```env
PORT=4000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password

AI_API_KEY=your_ai_api_key
```

Then start the backend:

```bash
npm start
```

For development:

```bash
npm run dev
```

Backend server:

```text
http://localhost:4000
```

---

# 💻 Frontend Setup

Open another terminal:

```bash
cd frontend
npm install
```

The frontend uses:

```env
VITE_API_URL=http://localhost:4000
```

Start the frontend:

```bash
npm run dev
```

The Vite development server will normally run on:

```text
http://localhost:5173
```

---

# 🔐 Environment Variables

**Never commit secret keys or `.env` files to GitHub.**

Recommended `.gitignore`:

```gitignore
node_modules/
.env
.env.*
dist/
uploads/
```

Before pushing the project to GitHub, make sure all API keys, database credentials, JWT secrets and Cloudinary credentials are removed from tracked files.

---

# 🖥️ Main Frontend Components

### Home

```text
components/Home.jsx
```

Main landing page of the application.

### Restaurant

```text
components/Restaurant.jsx
```

Displays restaurant-related information.

### Menu

```text
components/Menu.jsx
```

Displays available menus and food items.

### Food Item

```text
components/Fooditem.jsx
```

Handles individual food item presentation.

### Cart

```text
components/cart/Cart.jsx
```

Manages the user's shopping cart.

### Orders

```text
components/order/
```

Includes:

* Order List
* Order Details
* Order Success

### User

```text
components/user/
```

Includes:

* Login
* Register
* Profile
* Update Profile

---

# 🧠 Redux Architecture

The frontend uses Redux for centralized application state management.

```text
redux/
│
├── actions/
│   ├── cartActions.js
│   ├── menuActions.js
│   ├── orderActions.js
│   ├── restaurantAction.js
│   └── userActions.js
│
├── slices/
│   ├── cartSlice.js
│   ├── menuSlice.js
│   ├── orderSlice.js
│   ├── restaurantSlice.js
│   └── userSlice.js
│
└── store.js
```

This keeps user, cart, restaurant, menu and order state organized across the application.

---

# 📸 Screenshots

Add screenshots of the actual application here:

### 🏠 Home Page

```text
Add screenshot here
```

### 🍽️ Restaurant / Menu

```text
Add screenshot here
```

### 🍕 Food Items

```text
Add screenshot here
```

### 🛒 Cart

```text
Add screenshot here
```

### 📦 Orders

```text
Add screenshot here
```

### 🤖 AI Food Assistant

```text
Add screenshot here
```

### 👤 User Profile

```text
Add screenshot here
```

---

# 🚀 Future Improvements

* 🤖 Advanced personalized AI recommendations
* 🎙️ Voice-based food ordering
* 📍 Real-time order tracking
* 🔔 Real-time order notifications
* ⭐ Advanced food review system
* ❤️ Wishlist functionality
* 📱 Dedicated mobile application
* 🌐 Multi-language support
* 💳 More payment options
* 📊 Advanced restaurant analytics
* 🧠 Improved AI review sentiment analysis

---

# 🤝 Contributing

Contributions are welcome!

### 1. Fork the repository

### 2. Create a new branch

```bash
git checkout -b feature/new-feature
```

### 3. Make your changes

### 4. Commit your changes

```bash
git add .
git commit -m "Add new feature"
```

### 5. Push the branch

```bash
git push origin feature/new-feature
```

### 6. Create a Pull Request

---

# 📄 License

This project is created for **educational, learning and portfolio purposes**.

---

# 👨‍💻 Developer

**Mohammad Musharraf**

**MERN Stack Developer**

### ⭐ Support

If you found this project useful, please consider giving the repository a ⭐ on GitHub.
