# Bus Ticket Booking System (BACKEND)

## 🚀 Overview
The **Bus Ticket Booking System** is a web-based application that allows users to book bus tickets, manage rides, and receive email notifications for ticket purchases and verification.

## 🛠 Features
- **User Authentication** (Signup, Login, Email Verification)
- **Bus Ride Management** (Create, Update, and Cancel Rides)
- **Seat Availability & Booking**
- **QR Code Generation for Tickets**
- **Email Notifications** (User Verification & Ticket Confirmation)
- **Secure JWT Authentication**

## 📌 Tech Stack
- **Backend:** Node.js, Express.js, MongoDB, Mongoose
- **Authentication:** JWT, bcrypt
- **Email Service:** Nodemailer
- **QR Code Generation:** `qrcode` package
- **Validation:** Joi, Express Validator
- **Environment Configuration:** dotenv

## 📂 Project Structure
```
📦 Bus-Ticket-Booking-System-main
├── 📁 config          # Configuration files (DB, email, etc.)
├── 📁 controllers     # API controllers for handling requests
├── 📁 models          # Mongoose schemas/models
├── 📁 routes          # Express routes for different endpoints
├── 📁 middleware      # Authentication & validation middleware
├── 📁 utils           # Helper functions (QR Code, Email templates, etc.)
├── server.js          # Main entry point
├── package.json       # Dependencies and scripts
└── .env.example       # Example environment variables
```

## ⚙️ Installation & Setup
### 1️⃣ Clone the repository
```sh
git clone https://github.com/Faizan11khan/bus-ticket-booking-.git
cd bus-ticket-booking-
```

### 2️⃣ Install dependencies
```sh
npm install
```

### 3️⃣ Configure environment variables
Create a `.env` file in the root directory and add:
```env
# App settings
PORT=5000
NODE_ENV=development

# MongoDB connection
DATABASE=mongodb+srv://<username>:<password>@cluster0.mongodb.net/busbooking?retryWrites=true&w=majority&appName=Cluster0

# JWT settings
JWT_SECRET=your-jwt-secret-key
JWT_EXPIRES_IN=7d

# Stripe (for payments)
STRIPE_SECRET_KEY=your-stripe-secret-key

# Email SMTP settings (Mailtrap or other service)
EMAIL_HOST=smtp.mailtrap.io
EMAIL_PORT=2525
EMAIL_USER=your-mailtrap-username
EMAIL_PASS=your-mailtrap-password
EMAIL_FROM="Bus Ticketing <noreply@busbooking.com>"

# App URLs
PROD_URL=http://your-production-url.com
DEV_URL=http://localhost:3000

```

### 4️⃣ Start the server
```sh
npm start
```
The server will run at `http://localhost:5000`

## 🔥 API Endpoints
| Method | Endpoint                   | Description |
|--------|----------------------------|-------------|
| POST   | /api/users/register        | Register a new user |
| POST   | /api/users/login           | User login |
| GET    | /api/users/verify/:token   | Email verification |
| GET    | /api/rides                 | Get all available rides |
| POST   | /api/bookings              | Book a ride |
| GET    | /api/bookings/:id          | Get booking details |

## 📧 Email Templates
- **Account Verification Email**: Sent after registration with a verification link.
- **Ticket Confirmation Email**: Sent after successful ticket purchase with QR Code attachment.

## 🛡 Security Measures
- Password hashing using `bcrypt`
- JWT authentication for protected routes
- Input validation with `Joi`

## 🤝 Contributing
1. Fork the repository
2. Create a new branch (`feature/your-feature`)
3. Commit your changes
4. Push to your branch
5. Open a Pull Request

## 📜 License
This project is open-source and available under the **MIT License**.

---
🚀 Happy Coding! If you have any questions, feel free to open an issue!
