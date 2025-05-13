# 🧱 Multi-Service App (Auth + Users + API Gateway)

מערכת מבוססת Microservices שנבנתה עם Docker, Node.js ו־MongoDB, כולל פריסה חיה ל־Render.

---

## 🔧 מבנה המערכת

Client → API Gateway (port 3000)
├── /auth/register → Auth Service (port 3001, MongoDB)
└── /users → User Service (port 3002)

| Service        | טכנולוגיה        | פורט  | סטטוס |
|----------------|------------------|-------|--------|
| Auth Service   | Node.js + Mongo  | 3001  | ✅ פעיל |
| User Service   | Node.js בלבד     | 3002  | ✅ פעיל |
| API Gateway    | Express Proxy    | 3000  | ✅ פעיל |
| Database       | MongoDB (docker) | 27017 | ✅ פעיל |

---

## 🚀 איך מריצים לוקלית (Docker Compose)

```bash
git clone https://github.com/taltal1131/multi-service-app.git
cd multi-service-app
docker-compose up --build
🌐 מסלולים זמינים
🔹 POST /auth/register
{
  "email": "user@example.com",
  "password": "123456"
}
🔹 GET /users
[
  { "id": 1, "name": "Alice" },
  { "id": 2, "name": "Bob" }
]
🛠 טכנולוגיות
Node.js

Express

MongoDB

Docker

Docker Compose

