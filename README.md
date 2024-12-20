# Camp Server

This is a backend server for a camp management application. It provides APIs for managing camps, users, feedback, and payments.

> **[Client side](https://github.com/samwaseee/Care_Camp_client)**

## Features
- **Camp Management**: Create, read, update, and delete camps with sorting and filtering options.
- **User Management**: Manage user data, including roles and authentication.
- **Feedback**: Collect and retrieve feedback from users.
- **Payment Integration**: Integrated with Stripe for secure payments.
- **Authentication**: JWT-based authentication and authorization.
- **Middleware**: CORS and JSON parsing.

## Technologies Used
- **Node.js**: Runtime environment.
- **Express**: Web framework.
- **MongoDB**: Database.
- **Stripe**: Payment processing.
- **JWT**: Authentication and authorization.

## Setup Instructions
1. Clone this repository.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up a `.env` file with the following variables:
   ```env
   PORT=5000
   DB_USER=<your-mongodb-username>
   DB_PASS=<your-mongodb-password>
   STRIPE_SECRET_KEY=<your-stripe-secret-key>
   ACCESS_TOKEN_SECRET=<your-jwt-secret>
   ```
4. Start the server:
   ```bash
   node server.js
   ```

## API Endpoints
### Authentication
- `POST /jwt`: Generate a JWT token for authentication.

### Camps
- `GET /camps`: Retrieve all camps with sorting and filtering options.
- `GET /camps/:id`: Retrieve a single camp by ID.
- `POST /camps`: Create a new camp.
- `PATCH /camps/:id`: Update an existing camp.
- `DELETE /camps/:id`: Delete a camp.

### Users
- `GET /users`: Retrieve all users.
- `GET /users/admin/:email`: Check if a user is an admin.
- `POST /users`: Create a new user.

### Payments
- `POST /create-payment-intent`: Create a payment intent for Stripe.
- `GET /payments/:email`: Retrieve payments by email.
- `POST /payments`: Record a payment.

### Feedback
- `GET /feedbacks`: Retrieve all feedback.
- `POST /feedbacks`: Submit feedback.

### Middleware
- **CORS**: Restricted origins for secure communication.
- **JWT Authentication**: Protect routes and verify user roles.

## Deployment
This server is designed to run in a production environment. Ensure `NODE_ENV` is set to `production` for secure settings.
