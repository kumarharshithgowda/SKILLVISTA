Here is a **clean, updated README.md** for **SkillVista**, modified exactly as you asked — using **PostgreSQL (DB: Postgres)** instead of MongoDB.

You can directly paste this into your GitHub.

---

# **SKILLVISTA – FULL-STACK PROFESSIONAL NETWORKING PLATFORM**

SkillVista is a full-stack professional networking application inspired by platforms like LinkedIn.
It includes user authentication, job posting, and a dynamic dashboard.
The backend is powered by **Node.js + Express**, with **PostgreSQL** as the database and **EJS** templates for rendering dynamic pages.

---

## ⭐ **Features**

* **User Authentication**

  * Secure registration & login
  * Password hashing
  * Session management
* **Dashboard**

  * Displays user-specific home page
  * Reusable navigation components
* **Job Posting**

  * Users can create job posts
  * Stored and fetched from **PostgreSQL**
* **Dynamic Templating**

  * EJS for server-side rendered UI
  * Clean, consistent layout using partials
* **Robust Backend**

  * Express routing
  * PostgreSQL queries for CRUD operations

---

## 🛠 **Tech Stack**

### **Frontend**

* **EJS** (templating)
* **CSS** (custom styles)
* **Static assets** (images, layouts)

### **Backend**

* **Node.js**
* **Express.js**

### **Database**

* **PostgreSQL**
* Querying using:

  * `pg` (node-postgres driver)
  * SQL CRUD operations

### **Other Tools**

* Nodemon
* dotenv
* Morgan
* Git & GitHub

---

## 📁 **Project Structure**

```
SKILLVISTA/
│── app.js / server.js          # Main server file
│── package.json
│── public/
│   ├── styles.css
│   ├── images/
│   ├── bhanu/
│   └── rama/
│
│── views/
│   ├── login.ejs
│   ├── register.ejs
│   ├── home.ejs
│   ├── post-job.ejs
│   ├── secrets.ejs
│   └── partials/
│       ├── header.ejs
│       └── footer.ejs
│
│── db/
│   └── config.js               # PostgreSQL connection (pg Pool)
│
│── routes/ (optional)
│── controllers/ (optional)
```

---

## 🔧 **Environment Variables (`.env`)**

Create a `.env` file:

```
DB_HOST=localhost
DB_PORT=5432
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=skillvista
SESSION_SECRET=your_secret_key
```

---

## 🗄️ **PostgreSQL Table Structure**

### **Users Table**

```
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(100),
    email VARCHAR(150) UNIQUE,
    password VARCHAR(200)
);
```

### **Jobs Table**

```
CREATE TABLE jobs (
    id SERIAL PRIMARY KEY,
    company VARCHAR(150),
    position VARCHAR(150),
    description TEXT,
    user_id INT REFERENCES users(id)
);
```

---

## ▶️ **How to Run Locally**

### **1️⃣ Install dependencies**

```
npm install
```

### **2️⃣ Start server**

```
npm start
```

### **3️⃣ Ensure PostgreSQL is running**

Create database:

```
CREATE DATABASE skillvista;
```

Import tables (from SQL above).

---

## 🚀 **Future Enhancements**

* User profile update
* Direct messaging
* Media uploads
* Job recommendations
* Search functionality

---

## 🤝 **Contributing**

Pull requests and improvements are welcome!

---

