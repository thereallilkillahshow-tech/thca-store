
Built by https://www.blackbox.ai

---

# THCA Store

## Project Overview
THCA Store is a real-time eCommerce platform designed specifically for selling THCA products. The application includes robust back-end functionality, including user authentication, product management, and order processing, using a SQLite database for storage. It provides an API for easy integration and interaction with front-end applications or third-party services.

## Installation

To get started with THCA Store, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/thca-store-real.git
   cd thca-store-real
   ```

2. **Install the dependencies:**
   ```bash
   npm install
   ```

3. **Create a `.env` file** in the root directory and add the following environment variables:
   ```
   PORT=8000
   JWT_SECRET=your-secret-key
   ```

4. **Initialize the database:**
   This step sets up the necessary database tables.
   ```bash
   npm run init-db
   ```

5. **Start the application:**
   ```bash
   npm start
   ```

**For Development**: Use Nodemon for real-time server updates during development.
```bash
npm run dev
```

## Usage
Once the application is running, you can access the service at `http://localhost:8000`. You can interact with the API using tools like Postman or cURL to test various endpoints for user registration, login, product management, cart, and orders.

### API Endpoints
- **User Authentication**
  - Register User: `POST /api/auth/register`
  - Login User: `POST /api/auth/login`
  
- **Products**
  - Get Products: `GET /api/products`
  - Get Product by ID: `GET /api/products/:id`
  - Admin: Add, Update, and Delete products
  
- **Cart Management**
  - Get Cart: `GET /api/cart`
  - Add to Cart: `POST /api/cart`
  - Update Cart Item: `PUT /api/cart/:id`
  - Remove from Cart: `DELETE /api/cart/:id`
  
- **Orders**
  - Create Order: `POST /api/orders`
  - Get User Orders: `GET /api/orders`
  - Admin: Get all orders

## Features
- **User Registration and Authentication** with JWT tokens for secured API access.
- **Product Management** with admin access to add, update, or remove products.
- **Shopping Cart** for managing selected products before checkout.
- **Order Processing** to facilitate customer purchases with inventory checks.

## Dependencies
The project relies on the following dependencies:
- `express`: ^4.18.2 - Web framework for Node.js
- `sqlite3`: ^5.1.6 - SQLite database driver
- `bcryptjs`: ^2.4.3 - Password hashing
- `jsonwebtoken`: ^9.0.2 - JSON Web Token implementation
- `cors`: ^2.8.5 - Cross-Origin Resource Sharing middleware
- `helmet`: ^7.1.0 - Security middleware
- `express-rate-limit`: ^7.1.5 - Rate limiting middleware
- `multer`: ^1.4.5-lts.1 - Middleware for handling multipart/form-data
- `uuid`: ^9.0.1 - UUID utility for unique IDs
- `dotenv`: ^16.3.1 - Environment variable loader
- `axios`: ^1.6.2 - Promise-based HTTP client

### Development Dependencies
- `nodemon`: ^3.0.2 - Development tool to automatically restart the server during changes.

## Project Structure
```
/
├── public/                # Static files served by the application
├── scripts/               # Database initialization and seeding scripts
├── node_modules/         # Installed dependencies
├── server.js             # Entry point for the backend server
├── package.json          # Project metadata and dependencies
└── .env                  # Environment variables file
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.