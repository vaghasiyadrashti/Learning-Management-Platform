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

## 📌 Backend API Routes  

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


### **🚀Frontend Routes**


### **🚀 Public Routes (Accessible to All Users)**  
These routes can be accessed without logging in.  

🔹 **Home Page** → `/`  
🔹 **About Page** → `/about`  
🔹 **Browse Courses** → `/courses`  
🔹 **Register a New Account** → `/register`  
🔹 **Login to Your Account** → `/login`  
🔹 **Forgot Password** → `/forgot/password`  
🔹 **Reset Password (via Email Token)** → `/reset/password/:resetToken`  

---

### **🔐 User Routes (Only Accessible After Login)**  
Once logged in, users gain access to these features:  

 **View Profile** → `/user/profile`  
 **Edit Profile** → `/user/edit-profile`  
 **Change Password** → `/user/change-password`  
 **View a Specific Course** → `/course/:courseId`  
 **View Purchased Courses** → `/user/courses`  

---

### **🛠️ Admin Routes (Only Accessible by Admins)**  
Admins have additional privileges to manage courses and platform data:  

🔹 **Create a New Course** → `/course/create`  
🔹 **Update Course Details** → `/course/update`  
🔹 **Add Lecture to Course** → `/course/lecture/add`  
🔹 **Update Lecture Content** → `/course/lecture/update`  
🔹 **Admin Dashboard** → `/admin/dashboard`  

---

### **💳 Payment Gateway (For Course Purchases)**  
Users can securely purchase courses through these routes:  

🔹 **Proceed to Checkout** → `/checkout`  
🔹 **Payment Successful** → `/payment/success`  
🔹 **Payment Failed** → `/payment/failure`  

---

### **⚠️ Error Handling**  
If something goes wrong, the system provides appropriate error responses:  

 **Page Not Found (404)** → `*`  
 **Access Denied (403 - Unauthorized Access)** → `/denied`  
 **Internal Server Error (500)** → `/error`  

---
