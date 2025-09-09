# 🛍️ E-Commerce Platform – Full-Stack Online Store

A comprehensive, full-stack e-commerce application built with the MERN stack (MongoDB, Express.js, React, Node.js). This platform provides a complete online retail experience, featuring a dynamic shopping cart, secure payment processing with Stripe, and a full-featured admin dashboard for product management and sales analytics.

[LIVE LINK: https://e-commerce-platform-full-stack-online.onrender.com]

## ✨ Features

### 👑 Admin Features

  * **Product Management**: Create, update, and delete products from the store inventory.
  * **Featured Products**: Toggle a product's "featured" status to highlight it on the homepage.
  * **Sales Analytics**: View a detailed dashboard with key metrics like total users, total sales, total revenue, and daily sales charts.

### 👤 Customer Features

  * **Robust Authentication**: Secure user signup and login system using JWTs with access and refresh tokens.
  * **Product Browsing**: Explore products by category or view a carousel of featured items.
  * **Dynamic Shopping Cart**: Add products to the cart, update item quantities, or remove them entirely.
  * **Secure Checkout**: A seamless and secure payment process powered by Stripe.
  * **Coupon System**: Apply discount codes to the shopping cart for a percentage off the total price.

## 🛠️ Tech Stack

| Category                  | Technology                                                                                                                                                                                                                         |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Frontend** | **React**, **Zustand**, **Tailwind CSS**, **Framer Motion**, **Vite**                                                                |
| **Backend** | **Node.js**, **Express.js**                                                                                                                                                                       |
| **Database** | **MongoDB** (with Mongoose), **Redis** (for Caching)                                                                                                                     |
| **Services & APIs** | **Stripe** (Payments), **Cloudinary** (Image Storage)                                                                                                                                  |
| **Authentication** | **JSON Web Tokens (JWT)**, **bcryptjs**, **Cookie-Parser**                                                                                                    |

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

  * Node.js (v18 or later)
  * npm
  * MongoDB instance (local or cloud-based like MongoDB Atlas)
  * Redis instance (local or cloud-based like Upstash)

### Installation

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/shekharshekharraj/E-Commerce-Platform-Full-Stack-Online-Store.git
    cd E-Commerce-Platform-Full-Stack-Online-Store
    ```

2.  **Install Backend Dependencies:**

    ```sh
    npm install
    ```

3.  **Install Frontend Dependencies:**

    ```sh
    npm install --prefix frontend
    ```

4.  **Set Up Environment Variables:**
    Create a `.env` file in the root of the project and add the necessary variables. See the section below for details.

5.  **Run the Development Server:**
    This command starts both the backend server and the frontend Vite server concurrently.

    ```sh
    npm run dev
    ```

      * The backend will be available at `http://localhost:5000`.
      * The frontend will be available at `http://localhost:5173`.

## 🔒 Environment Variables

You need to create a `.env` file in the root directory and add the following variables. All of these are essential for the application to run.

```env
PORT=5000
MONGO_URI=<YOUR_MONGODB_CONNECTION_STRING>
UPSTASH_REDIS_URL=<YOUR_UPSTASH_REDIS_URL>

ACCESS_TOKEN_SECRET=<YOUR_ACCESS_TOKEN_SECRET>
REFRESH_TOKEN_SECRET=<YOUR_REFRESH_TOKEN_SECRET>

CLOUDINARY_CLOUD_NAME=<YOUR_CLOUDINARY_CLOUD_NAME>
CLOUDINARY_API_KEY=<YOUR_CLOUDINARY_API_KEY>
CLOUDINARY_API_SECRET=<YOUR_CLOUDINARY_API_SECRET>

STRIPE_SECRET_KEY=<YOUR_STRIPE_SECRET_KEY>

CLIENT_URL=http://localhost:5173
NODE_ENV=development
```

## 📝 API Endpoints

A brief overview of the main API routes available.

| Method   | Endpoint                          | Description                                         | Protected | Admin Only |
| -------- | --------------------------------- | --------------------------------------------------- | --------- | ---------- |
| `POST`   | `/api/auth/signup`                | Register a new user.                                | No        | No         |
| `POST`   | `/api/auth/login`                 | Log in a user.                                      | No        | No         |
| `GET`    | `/api/auth/profile`               | Get the current user's profile.                     | Yes       | No         |
| `GET`    | `/api/products`                   | Get a list of all products.                         | Yes       | Yes        |
| `POST`   | `/api/products`                   | Create a new product.                               | Yes       | Yes        |
| `DELETE` | `/api/products/:id`               | Delete a product.                                   | Yes       | Yes        |
| `GET`    | `/api/cart`                       | Get the contents of the user's cart.                | Yes       | No         |
| `POST`   | `/api/cart`                       | Add a product to the cart.                          | Yes       | No         |
| `GET`    | `/api/analytics`                  | Get sales and user analytics data.                  | Yes       | Yes        |
| `POST`   | `/api/payments/create-checkout`   | Create a new Stripe checkout session.               | Yes       | No         |

##Author: Raj Shekhar
