# 🎓 Learning Management Platform (LMP)  
Built using **Express.js** and **MongoDB**. It provides APIs for user authentication, course management, user progress tracking, payments, and admin analytics.  

## 🚀 Features  
 User Authentication (Register, Login, Password Reset)  
 Course & Lecture Management (CRUD by Admin)  
 User Progress Tracking  
 Secure Payment Integration (Checkout & Verification)  
 Admin Dashboard for Course Sales Analytics  

---

## 🛠️ Tech Stack  
- **Backend:** Node.js, Express.js  
- **Database:** MongoDB  
- **Authentication:** JWT & Bcrypt  
- **Payment Gateway:** Stripe  
- **Storage:** Cloudinary (for media files)  

---

## 📌 API Routes  

### 🔐 User Authentication (`/api/v1/user`)  
| Method | Route | Description |
|--------|-------|-------------|
| POST   | `/register` | Register a new user |
| POST   | `/login` | Login user |
| GET    | `/me` | Get user details |
| PUT    | `/me` | Update user details |
| GET    | `/logout` | Logout user |
| POST   | `/reset` | Forgot password request |
| POST   | `/reset/:resetToken` | Reset password using token |
| PUT    | `/change-password` | Change password |

---

### 📚 Courses & Lectures (`/api/v1/course`)  
| Method | Route | Description |
|--------|-------|-------------|
| GET    | `/category` | Get all course categories |
| GET    | `/instructor` | Get instructor details |
| POST   | `/` | Create a new course (Admin only) |
| GET    | `/` | Get all courses |
| PUT    | `/:courseId` | Update a course (Admin only) |
| DELETE | `/:courseId` | Delete a course (Admin only) |

---

### 📈 User Progress (`/api/v1/my-course`)  
| Method | Route | Description |
|--------|-------|-------------|
| GET    | `/` | Get user’s purchased courses |
| POST   | `/:courseId` | Track user progress |
| PUT    | `/:courseId` | Update user progress |
| DELETE | `/:courseId` | Remove user from course |

---

### 💰 Payment Gateway (`/api/v1/payment`)  
| Method | Route | Description |
|--------|-------|-------------|
| GET    | `/getkey` | Get API key for payments |
| POST   | `/checkout` | Start payment process |
| POST   | `/verify` | Verify payment & grant access |

---

### 🏆 Admin Dashboard (`/api/v1/admin`)  
| Method | Route | Description |
|--------|-------|-------------|
| GET    | `/courses-sell-by-user` | Get course sales by user |
| GET    | `/courses-sell-by-course` | Get course sales by course |

---

## 🔧 Installation & Setup  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2️⃣ Install Dependencies  
```bash
npm install
```

### 3️⃣ Set Up Environment Variables  
Create a `.env` file and add the following:  
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
SMTP_USER=your_smtp_email
SMTP_PASS=your_smtp_password
PAYMENT_KEY=your_payment_gateway_key
```

### 4️⃣ Run the Server  
```bash
npm start
```
The API will be running at `http://localhost:5000`.

---
