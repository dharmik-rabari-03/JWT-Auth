<div align="center">

# 🔐 JWT Authentication API

<img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=30&pause=1000&color=00F7FF&center=true&vCenter=true&width=700&lines=Node.js+JWT+Authentication;Express.js+%7C+MongoDB+%7C+Mongoose;Secure+Login+%7C+Authentication+API" />

<p align="center">
<img src="https://img.shields.io/badge/Node.js-20+-green?style=for-the-badge&logo=node.js"/>
<img src="https://img.shields.io/badge/Express.js-Backend-black?style=for-the-badge&logo=express"/>
<img src="https://img.shields.io/badge/MongoDB-Database-green?style=for-the-badge&logo=mongodb"/>
<img src="https://img.shields.io/badge/JWT-Authentication-orange?style=for-the-badge&logo=jsonwebtokens"/>
<img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge"/>
</p>

</div>

---

# 📖 About Project

This project is a **JWT Authentication REST API** built using **Node.js**, **Express.js**, **MongoDB**, and **Mongoose**.

It allows users to:

- 👤 Register
- 🔑 Login
- 🔒 Authenticate using JWT Token
- ✏️ Update Profile
- 🚪 Logout Current Device
- 🌍 Logout from All Devices
- 🗑 Delete User
- 📋 View All Users

Passwords are securely encrypted using **bcryptjs**, and authentication is handled using **JSON Web Tokens (JWT).**

---

# 🚀 Tech Stack

| Technology | Purpose |
|------------|----------|
| Node.js | Backend Runtime |
| Express.js | REST API Framework |
| MongoDB | Database |
| Mongoose | ODM |
| JWT | Authentication |
| bcryptjs | Password Hashing |
| dotenv | Environment Variables |
| Nodemon | Development |

---

# 📂 Project Structure

```
JWT_Authentication/
│
├── config/
│      db.js
│
├── controller/
│      userController.js
│
├── middleware/
│      auth.js
│      httpError.js
│
├── model/
│      userModel.js
│
├── routes/
│      userRoute.js
│
├── .env
├── server.js
├── package.json
└── README.md
```


---

## 1️⃣ Add User

### POST `/add`

Register a new user.

### Request

```json
{
"name":"Dharmik",
"Email":"dharmik@gmail.com",
"password":"12345678"
}
```

### Response

```json
{
"message":"User Added Successfully"
}
```

📷 Screenshot

<img width="821" height="650" alt="image" src="https://github.com/user-attachments/assets/a8625aba-2974-424e-b76d-07022c5e6a26" />



---

## 2️⃣ Login

### POST `/login`

Authenticate user and generate JWT Token.

### Request

```json
{
"Email":"dharmik@gmail.com",
"password":"12345678"
}
```

### Response

```json
{
"user":{},
"token":"JWT TOKEN"
}
```

📷 Screenshot


<img width="1170" height="671" alt="image" src="https://github.com/user-attachments/assets/3959cc6b-53af-4714-8807-1c1c8b67732c" />



---

## 3️⃣ Auth Login

### GET `/authlogin`

Requires JWT Token.

Header

```
Authorization

Bearer TOKEN
```

Returns authenticated user.

📷 Screenshot


<img width="853" height="666" alt="image" src="https://github.com/user-attachments/assets/0540d24e-f32f-4fae-9c94-0afbdc7e4e7c" />



---

## 4️⃣ Get All Users

### GET `/getAllUser`

Returns all registered users.

📷 Screenshot


<img width="814" height="780" alt="image" src="https://github.com/user-attachments/assets/79164b5f-04a2-4313-9e35-d79589524818" />



---

## 5️⃣ Update User

### PATCH `/update/:id`

Update user information.

Example

```json
{
"name":"New Name"
}
```

📷 Screenshot


<img width="1080" height="691" alt="image" src="https://github.com/user-attachments/assets/6b235dae-2c1a-4d61-bebc-9681324ae3d6" />



---

## 6️⃣ Logout

### GET `/logout`

Logout current device.

JWT Token Required.

📷 Screenshot


<img width="861" height="593" alt="image" src="https://github.com/user-attachments/assets/1080fbf3-4d01-40f2-a852-f402d4aaf898" />



---

## 7️⃣ Logout All

### GET `/logoutAll`

Removes all active JWT Tokens.

JWT Token Required.

📷 Screenshot


<img width="1026" height="544" alt="image" src="https://github.com/user-attachments/assets/ee3aac05-123f-4b3b-8cb0-e7062a0b3754" />



---

## 8️⃣ Delete User

### DELETE `/delete/:id`

Delete user by ID.

JWT Token Required.

📷 Screenshot


<img width="866" height="546" alt="image" src="https://github.com/user-attachments/assets/8f71484f-e226-4e46-baca-f971c07aa87f" />



---

# 🔐 JWT Authentication Flow

```text
User
 │
 │ Register
 ▼
MongoDB
 │
 │ Login
 ▼
JWT Token Generated
 │
 ▼
Client Stores Token
 │
 ▼
Authorization Header
Bearer Token
 │
 ▼
Auth Middleware
 │
 ▼
Verify JWT
 │
 ▼
Protected Routes
```

---

# 🛡 Authentication

Protected Routes require

```
Authorization

Bearer YOUR_TOKEN
```

---

# 📦 Dependencies

```json
bcryptjs

dotenv

express

jsonwebtoken

mongoose

nodemon
```

---

# ⭐ Features

✅ JWT Authentication

✅ Password Hashing

✅ Secure Login

✅ Protected Routes

✅ Logout Current Device

✅ Logout All Devices

✅ CRUD Operations

✅ MongoDB Integration

✅ REST API

---

# 👨‍💻 Author

### Dharmik

Full Stack Developer

---

<div align="center">


Made with ❤️ using Node.js

</div>
