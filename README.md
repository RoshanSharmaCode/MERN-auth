# 🔐 MERN Auth

A full-stack authentication system built with the **MERN Stack** featuring secure user authentication, email verification using OTP, and password reset functionality.

## 🚀 Features

- 👤 User Registration
- 🔑 User Login & Logout
- ✅ Email Verification with 6-digit OTP
- 🔒 Secure Password Reset via Email
- 🔐 JWT Authentication
- 🍪 HTTP-Only Cookie-based Authentication
- 🔑 Password Hashing with Bcrypt
- 📧 Professional HTML Email Templates
- 📱 Responsive UI with Tailwind CSS
- 🔔 Toast Notifications

---

## 🛠️ Tech Stack

### Frontend
- React.js
- Vite
- Tailwind CSS
- React Router DOM
- Axios
- React Toastify
- Context API

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- Bcrypt.js
- Cookie Parser
- Nodemailer
- Brevo SMTP
- Dotenv

---

## 📂 Project Structure

```
mern-auth/
│
├── client/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── templates/
│   ├── server.js
│   └── package.json
│
└── README.md
```

---

## ⚡ Authentication Flow

### Registration
- User registers with name, email, and password.
- Password is securely hashed using **Bcrypt**.
- User account is created in MongoDB.
- A JWT token is generated and stored in an **HTTP-only cookie**.

### Email Verification
- A 6-digit OTP is generated.
- OTP is emailed to the user using **Nodemailer + Brevo SMTP**.
- User enters the OTP.
- Email is verified after successful validation.

### Login
- User logs in using email and password.
- Password is verified using Bcrypt.
- JWT token is generated.
- Authentication cookie is stored securely.

### Logout
- JWT cookie is cleared.
- User session ends.

### Forgot Password
- User requests password reset.
- Reset OTP is emailed.
- User verifies OTP.
- New password is hashed and updated in the database.

---

## 📧 Email Features

- Beautiful HTML Email Templates
- Email Verification OTP
- Password Reset OTP
- Professional Email Design
- Secure OTP Expiration

---

## 🔒 Security Features

- Password Hashing with Bcrypt
- JWT Authentication
- HTTP-Only Cookies
- Protected API Routes
- Email Verification
- OTP Expiration
- Environment Variables
- MongoDB Validation
- Secure Password Reset Flow

---

## ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/RoshanSharmaCode/MERN-auth.git
cd mern-auth
```

### Install Backend Dependencies

```bash
cd server
npm install
```

### Install Frontend Dependencies

```bash
cd ../client
npm install
```

---

## 🔑 Environment Variables

Create a `.env` file inside the **server** directory.

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_secret_key

NODE_ENV=development

SMTP_HOST=smtp-relay.brevo.com
SMTP_PORT=587
SMTP_USER=your_brevo_email
SMTP_PASS=your_brevo_smtp_key

SENDER_EMAIL=your_email@example.com

CLIENT_URL=http://localhost:5173
```

---

## ▶️ Running the Project

### Start Backend

```bash
cd server
npm run server
```

### Start Frontend

```bash
cd client
npm run dev
```

Frontend:

```
http://localhost:5173
```

Backend:

```
http://localhost:5000
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login user |
| POST | `/api/auth/logout` | Logout user |
| POST | `/api/auth/send-verify-otp` | Send verification OTP |
| POST | `/api/auth/verify-account` | Verify email |
| GET | `/api/auth/is-auth` | Check authentication |
| POST | `/api/auth/send-reset-otp` | Send password reset OTP |
| POST | `/api/auth/reset-password` | Reset password |

---

## 💻 Frontend Pages

- Home
- Login
- Register
- Email Verification
- Forgot Password
- Reset Password

---

## 📸 Screenshots

Add screenshots of:

- Home Page
  <img width="2854" height="1622" alt="image" src="https://github.com/user-attachments/assets/9225d87d-fdb0-4715-9d72-7feaac38f4ec" />

- Login Page
  
- Registration Page
  <img width="2782" height="1580" alt="image" src="https://github.com/user-attachments/assets/4a03b53e-9a86-485a-bcf6-fc53de1cad66" />

- Email Verification
  <img width="2784" height="1582" alt="image" src="https://github.com/user-attachments/assets/7098b3b8-f4c7-48a4-b50b-3be2b673b7cd" />

---

## ⭐ Show Your Support

If you found this project helpful, consider giving it a ⭐ on GitHub!
