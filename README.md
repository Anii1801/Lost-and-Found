# 🔍 Lost & Found Item Management System

A full-stack web application built with the **MERN Stack** that helps college students report and find lost or found items on campus.

---

## 🌐 Live Demo

- **Frontend:** `https://lost-and-found-frontend-znsy.onrender.com/`
- **Backend API:** `https://lost-and-found-backend-4t44.onrender.com/api`

---

## 📌 Features

- 🔐 User Registration & Login with JWT Authentication
- 📝 Report Lost or Found items with full details
- 📋 View all reported items on Dashboard
- 🔍 Search items by name
- ✏️ Update your own reported items
- 🗑️ Delete your own reported items
- 🚪 Secure Logout
- 🛡️ Protected routes — only logged-in users can access dashboard

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js, Axios, CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JWT (JSON Web Token), bcrypt |
| Deployment | Render (Backend), Vercel (Frontend) |

---

## 📁 Project Structure

```
lost-and-found/
│
├── backend/
│   ├── index.js          # Main server file
│   ├── .env              # Environment variables
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── App.jsx       # Main React component
│   │   └── App.css       # Styling
│   └── package.json
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/lost-and-found.git
cd lost-and-found
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend folder:
```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```

Start the backend server:
```bash
node index.js
```

### 3. Frontend Setup
```bash
cd frontend
npm install
npm start
```

---

## 🔗 API Endpoints

### Auth Routes
| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/register` | Register new user | ❌ |
| POST | `/api/login` | Login user, returns JWT | ❌ |

### Item Routes
| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/items` | Add new item | ✅ |
| GET | `/api/items` | Get all items | ✅ |
| GET | `/api/items/:id` | Get item by ID | ✅ |
| PUT | `/api/items/:id` | Update item | ✅ |
| DELETE | `/api/items/:id` | Delete item | ✅ |
| GET | `/api/items/search?name=xyz` | Search items by name | ✅ |
| GET | `/dashboard` | Protected dashboard route | ✅ |

---

## 🧪 Sample API Requests (Thunder Client / Postman)

### Register
```json
POST /api/register
{
  "name": "Priya Verma",
  "email": "priya.verma@college.edu",
  "password": "priya@2025"
}
```

### Login
```json
POST /api/login
{
  "email": "priya.verma@college.edu",
  "password": "priya@2025"
}
```

### Add Item (requires Bearer token in header)
```json
POST /api/items
{
  "itemName": "Blue Backpack",
  "description": "Navy blue bag with red zipper",
  "type": "Lost",
  "location": "Library, 2nd Floor",
  "date": "2025-04-20",
  "contactInfo": "9876543210"
}
```

---

## 🔐 Authentication

This project uses **JWT (JSON Web Token)** for authentication.

1. After login, a token is returned
2. Store the token in `localStorage`
3. Send it in the `Authorization` header for protected routes:
```
Authorization: Bearer <your_token>
```

---

## 📦 Dependencies

### Backend
```json
"dependencies": {
  "bcryptjs": "^2.4.3",
  "cors": "^2.8.5",
  "dotenv": "^16.0.3",
  "express": "^4.18.2",
  "jsonwebtoken": "^9.0.0",
  "mongoose": "^7.0.0"
}
```

### Frontend
```json
"dependencies": {
  "axios": "^1.4.0",
  "react": "^18.2.0",
  "react-dom": "^18.2.0"
}
```

---

## 🚀 Deployment

### Backend — Render
1. Push code to GitHub
2. Go to [render.com](https://lost-and-found-backend-4t44.onrender.com/api)
3. Create new **Web Service**
4. Connect your GitHub repo
5. Set environment variables (`MONGO_URI`, `JWT_SECRET`)
6. Deploy ✅

### Frontend —render
1. Push frontend code to GitHub
2. Go to [render.com](https://lost-and-found-frontend-znsy.onrender.com/)
3. Import your GitHub repo
4. Deploy ✅

---

## 👤 Author

**Your Name**
- GitHub: [Anii1801](https://github.com/Anii1801/Lost-and-Found/)
- Email: anurudhs06@email.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
