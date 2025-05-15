# 🧱 Multi-Service App (Auth + Users + API Gateway)

A microservices-based system built with **Node.js**, **MongoDB**, and **Docker**,  
featuring live deployment to **Render** and fully containerized services.

---

## 🧭 System Architecture

Client
│
▼
API Gateway (port 3000)
├── /auth/register → Auth Service (port 3001, MongoDB)
└── /users → User Service (port 3002)

yaml
Copy
Edit

---

## 🧩 Services Overview

| Service       | Technology         | Port   | Status     |
|---------------|--------------------|--------|------------|
| Auth Service  | Node.js + MongoDB  | 3001   | ✅ Active   |
| User Service  | Node.js (Express)  | 3002   | ✅ Active   |
| API Gateway   | Express Proxy      | 3000   | ✅ Active   |
| Database      | MongoDB (Docker)   | 27017  | ✅ Active   |

---

## 🚀 Running Locally (with Docker Compose)

```bash
git clone https://github.com/taltal1131/multi-service-app.git
cd multi-service-app
docker-compose up --build
Once running, access the following routes:

🌐 Available Endpoints
🔹 Auth Service
POST /auth/register

Request Body:

json
Copy
Edit
{
  "email": "user@example.com",
  "password": "123456"
}
🔹 User Service
GET /users

Response Example:

json
Copy
Edit
[
  { "id": 1, "name": "Alice" },
  { "id": 2, "name": "Bob" }
]
🛠 Technologies Used
Node.js

Express

MongoDB

Docker

Docker Compose

📄 License
This project is open-source and available under the MIT License.

<p align="center"> 🚀 Built by <a href="https://github.com/taltal1131">taltal1131</a> – Always Learning, Always Building! </p> ```
