# 🛒 Simple Shopping Cart

A full-stack e-commerce application with a TypeScript Express backend and React frontend with modern UI components.

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Tech Stack](#-tech-stack)
- [Live Demo](#-live-demo)
- [Quick Start](#-quick-start)
- [Backend Setup](#-backend-setup)
- [Frontend Setup](#-frontend-setup)
- [API Documentation](#-api-documentation)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Environment Variables](#-environment-variables)
- [Deployment](#-deployment)
- [Testing](#-testing)

## 🎯 Project Overview

A minimal e-commerce site that allows users to:

- Browse products in a responsive grid layout
- Add items to a shopping cart
- Manage cart quantities
- Simulate checkout process
- Persist cart data across browser sessions

## 🛠 Tech Stack

### Backend

- **Runtime**: Node.js
- **Language**: TypeScript
- **Framework**: Express.js
- **Security**: Helmet, CORS
- **Logging**: Morgan
- **Testing**: Jest, Supertest
- **Development**: Nodemon, ts-node

### Frontend

- **Framework**: React 18
- **Language**: TypeScript
- **Routing**: React Router DOM
- **UI Components**: shadcn/ui
- **Icons**: Lucide React
- **State Management**: React Context API
- **HTTP Client**: Fetch API
- **Notifications**: Sonner
- **Build Tool**: Vite

## 🌐 Live Demo

- **Frontend(Vercel)**: [https://verto-assignment-client.vercel.app/](https://verto-assignment-client.vercel.app/)
- **Backend API(Render)**: [https://verto-assignment-server.onrender.com/](https://verto-assignment-server.onrender.com/)

## 🚀 Quick Start

### Prerequisites

- Node.js 16+
- npm or yarn

### One-Command Setup

```bash
# Clone the repository
git clone <repository-url>
cd shopping-cart

# Install and run both frontend and backend
npm run setup:dev
```

## 🔧 Backend Setup

### Installation

```bash
cd backend
npm install
```

### Environment Setup

Create `.env` file in backend directory:

```env
PORT=5000
NODE_ENV=development
```

### Development

```bash
# Run in development mode with hot reload
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

### Testing

```bash
# Run tests
npm test

# Run tests in watch mode
npm run test:watch
```
<!-- 
## 🎨 Frontend Setup

### Installation

```bash
cd frontend
npm install
```

### Environment Setup

Create `.env` file in frontend directory:

```env
VITE_API_URL=http://localhost:5000/api
``` -->

### Development

```bash
# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📚 API Documentation

### Base URL

```
http://localhost:5000/api
```

### Endpoints

#### 🏥 Health Check

```http
GET /
```

**Response:**

```json
{
  "success": true,
  "timestamp": "2024-01-01T00:00:00.000Z",
  "service": "Shopping Cart API"
}
```

#### 📦 Products

```http
GET /products
```

**Response:**

```json
{
  "success": true,
  "message": "Products retrieved successfully",
  "data": [
    {
      "id": 1,
      "title": "Fjallraven - Foldsack No. 1 Backpack",
      "price": 109.95,
      "description": "Your perfect pack for everyday use...",
      "category": "men's clothing",
      "image": "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg",
      "rating": {
        "rate": 3.9,
        "count": 120
      }
    }
  ]
}
```

```http
GET /products/:id
```

**Parameters:**

- `id` (number): Product ID

#### 🛒 Checkout

```http
POST /checkout
```

**Request Body:**

```json
{
  "items": [
    {
      "id": 1,
      "quantity": 2
    },
    {
      "id": 2,
      "quantity": 1
    }
  ]
}
```

**Response:**

```json
{
  "success": true,
  "message": "Order processed successfully",
  "orderId": "ORD-1704067200000-abc123",
  "total": 242.9
}
```

## ✨ Features

### Core Features

- ✅ Product listing with responsive grid
- ✅ Add to cart functionality
- ✅ Cart management (add, remove, update quantities)
- ✅ Checkout simulation
- ✅ User session with name entry

### Bonus Features

- ✅ Cart persistence with localStorage
- ✅ Product category filtering
- ✅ Responsive design
- ✅ Modern UI with shadcn components
- ✅ Toast notifications
- ✅ Backend API tests

### User Experience

- 🎨 Clean, modern interface
- 📱 Mobile-responsive design
- ⚡ Fast loading with optimized images
- 🔄 Real-time cart updates
- 💾 Data persistence across sessions

## 📁 Project Structure

### Backend Structure

```
backend/
├── src/
│   ├── controllers/     # Route controllers
│   ├── routes/          # API routes
│   ├── types/           # TypeScript definitions
│   ├── utils/           # Utilities and mock data
│   └── app.ts          # Express app setup
├── tests/              # Test suites
├── dist/               # Compiled JavaScript
└── package.json
```

### Frontend Structure

```
frontend/
├── src/
│   ├── components/     # React components
│   │   ├── ui/        # shadcn/ui components
│   │   ├── Navbar.tsx
│   │   ├── ProductCard.tsx
│   │   ├── Cart.tsx
│   │   └── UserForm.tsx
│   ├── contexts/       # React Context
│   ├── pages/          # Page components
│   ├── types/          # TypeScript definitions
│   ├── lib/            # API utilities
│   └── App.tsx
├── public/             # Static assets
└── package.json
```

## 🔑 Environment Variables

### Backend (.env)

```env
PORT=5000
NODE_ENV=development
```

### Frontend (.env)

```env
VITE_API_URL=http://localhost:5000/api
```

## 🚀 Deployment

### Backend Deployment (Example: Railway/Render)

```bash
# Build the project
npm run build

# Start production server
npm start
```

### Frontend Deployment (Example: Vercel/Netlify)

```bash
# Build the project
npm run build

# The dist folder is ready for deployment
```

## 🧪 Testing

### Backend Tests

```bash
cd backend
npm test
```

Test coverage includes:

- Product endpoints
- Health check endpoint
- Error handling

### Frontend Testing

Manual testing recommended for:

- User flow (name entry → products → cart → checkout)
- Responsive design
- Cart persistence
- Error states

<div align="center">

**Built with ❤️ using Modern Web Technologies**

[Back to Top](#-simple-shopping-cart)

</div>
