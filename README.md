# Node.js + MongoDB API Demo

A simple REST API built with Node.js, Express, and MongoDB for product management.

## Table of Contents

- [About](#about)
- [Live Application Details](#live-application-details)
- [Tech Stack](#tech-stack)
- [API Endpoints](#api-endpoints)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)

## About

This project demonstrates a basic CRUD API for managing products. It includes endpoints to create and retrieve products with MongoDB Atlas integration using Mongoose ODM.

**Features:**
- Create new products
- Get all products
- Data validation
- MongoDB Atlas integration
- Ready for deployment

## Live Application Details

- **Live API Base URL:** https://node-mongodb-api-demo.onrender.com
- **Deployment Platform:** Render (Free Tier)
- **Database:** MongoDB Atlas (Cloud)

**API Postman Collection:** [node-mongodb-api-demo.postman_collection.json](./node-mongodb-api-demo.postman_collection.json)

## Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB Atlas
- **ODM:** Mongoose
- **Environment:** dotenv
- **Package Manager:** pnpm

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/products` | Create a new product |
| GET | `/api/products` | Get all products |

### Example Usage

**Create Product:**
```bash
curl -X POST http://localhost:5000/api/products \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Laptop",
    "description": "High-performance laptop for development",
    "price": 999.99,
    "category": "Electronics",
    "stock": 10
  }'
```

**Get All Products:**
```bash
curl http://localhost:5000/api/products
```

## Quick Start

1. **Install dependencies:**
   ```bash
   pnpm install
   ```

2. **Set up environment:**
   - Create `.env` file
   - Add your MongoDB Atlas connection string:
     ```
     MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/database_name
     ```

3. **Start the server:**
   ```bash
   # Development
   pnpm run dev
   
   # Production
   pnpm start
   ```

4. **Access the API:**
   - Server runs on `http://localhost:5000`
   - API endpoints available at `/api/products`

## Project Structure

```
node-mongodb-api-demo/
├── models/
│   └── Product.js          # Product schema and model
├── routes/
│   └── products.js         # Product routes
├── server.js               # Main server file
├── package.json            # Dependencies and scripts
└── README.md              # This file
```