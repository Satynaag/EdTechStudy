# 📚 StudyNotion – EdTech Platform

**Live Demo**: [https://Edtech-frontend-wheat.vercel.app/](https://ed-tech-study-668u.vercel.app/)

> **Note**: OTP verification email might be found in your **Spam** folder.

---

## 🌟 Overview

**StudyNotion** is a full-stack EdTech platform that enables students to browse, purchase, and take courses, while instructors can create and manage content efficiently. The platform features authentication, secure payment integration, media handling, and responsive UI.

---

## ⚙️ System Architecture

StudyNotion follows a **client-server architecture**:

- **Frontend**: Built with ReactJS (Client)
- **Backend**: Built with NodeJS + ExpressJS (Server)
- **Database**: MongoDB (Cloud Hosted)

---

## 🧠 Features

### 👨‍🎓 For Students

- Homepage with course previews
- Course browsing and wishlist
- Secure checkout and enrollment
- Watch video lectures and read materials
- Profile management and edit details

### 👨‍🏫 For Instructors

- Dashboard with course statistics
- Course creation, update, delete
- Manage lectures and pricing
- View feedback and insights

### 🔐 Core Backend Features

- OTP-based signup and login
- JWT authentication
- Password reset support
- Razorpay payment integration
- Cloudinary media storage
- Markdown-based document formatting

---

## 🛠️ Tech Stack

### Frontend

- ReactJS
- Redux Toolkit (State Management)
- TailwindCSS
- React Router

### Backend

- NodeJS
- ExpressJS
- MongoDB + Mongoose
- JWT (Authentication)
- Bcrypt (Password hashing)
- Cloudinary (Media)
- Razorpay (Payments)

---

## 📁 Folder Structure

```
studyNotion/
├── client/           # React frontend
└── server/           # Node.js backend
```

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Horror26/StudyNotion.git
cd StudyNotion
```

---

### 2. Frontend Setup

```bash
cd client
cp .env.example .env
npm install
npm start
```

> Make sure to replace the `.env` values with your actual environment variables.

---

### 3. Backend Setup

```bash
cd server
cp .env.example .env
npm install
npm run dev
```

> The backend will run on `http://localhost:4000` by default.

---

## 📬 API Usage Example (Using Postman)

### 🔹 a. Send OTP

```http
POST http://localhost:4000/api/v1/auth/sendotp

Body (JSON):
{
  "email": "testadmin@gmail.com"
}
```

### 🔹 b. Sign Up

```http
POST http://localhost:4000/api/v1/auth/signup

Body (JSON):
{
  "firstName": "test",
  "lastName": "admin",
  "email": "testadmin@gmail.com",
  "password": "123",
  "confirmPassword": "123",
  "accountType": "Admin",
  "otp": "<OTP from previous response>"
}
```

### 🔹 c. Login

```http
POST http://localhost:4000/api/v1/auth/login

Body (JSON):
{
  "email": "test@gmail.com",
  "password": "123"
}
```

### 🔹 d. Create Category

```http
POST http://localhost:4000/api/v1/course/createCategory

Body (JSON):
{
  "name": "Web DEV",
  "description": "MWEN STACK"
}
```

---

## 🧾 Data Models Overview

### 🧑 Student Schema

- First Name, Last Name
- Email, Password (Hashed)
- Enrolled Courses

### 🧑‍🏫 Instructor Schema

- Full Details
- Created Courses
- Instructor Dashboard

### 📚 Course Schema

- Title & Description
- Category & Instructor
- Media (Image, Video)
- Price, Rating

---

## 🌐 Database

- **MongoDB Atlas**: A NoSQL cloud database for fast, flexible document storage.

---

## 🤝 Contributing

🎉 **Hacktoberfest is ON!**  
We welcome contributions! Found a bug or have suggestions?  
→ [Open an issue](https://github.com/Horror26/StudyNotion/issues) or submit a pull request.

---

## 👨‍💻 Author

**Avinash (Horror26)**  
Feel free to connect or check out my other repositories!
