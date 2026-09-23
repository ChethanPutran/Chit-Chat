# 💬 Real-Time Chat Application

A full-stack real-time messaging web application built with modern web technologies. This application supports seamless instant messaging, active session handling, user authentication, and interactive chat features.

---

## 🚀 Features

- **Real-Time Messaging:** Instant bidirectional communication powered by WebSockets / Socket.io.
- **User Authentication & Authorization:** Secure user signup, login, and token-based session management (JWT / Cookies).
- **One-on-One & Group Chats:** Support for direct messaging between users as well as group conversations.
- **Online/Offline Status:** Live user presence indicators showing active users in real time.
- **Message History:** Persistent conversation history backed by a database.
- **Responsive UI:** Clean, intuitive UI/UX tailored for both mobile and desktop screens.

---

## 🛠️ Tech Stack

### **Frontend**
- **Framework/Library:** React / HTML5 & CSS3
- **Styling:** CSS3 / Tailwind CSS
- **State Management & Real-time:** Socket.io Client, Axios

### **Backend**
- **Runtime & Framework:** Node.js, Express.js
- **Real-Time Engine:** Socket.io
- **Database:** MongoDB (Mongoose ORM)
- **Authentication:** JSON Web Tokens (JWT) / bcryptjs

---

## 📁 Repository Structure

```text
Chat-App/
├── client/              # Frontend React application
│   ├── public/          # Static assets
│   └── src/             # Components, context, pages, and styles
├── server/              # Backend Express & Socket.io server
│   ├── config/          # Database & app configurations
│   ├── controllers/     # API request handlers
│   ├── middleware/      # Auth & validation middleware
│   ├── models/          # Mongoose schemas (User, Message, Chat)
│   ├── routes/          # Express route definitions
│   └── index.js         # Backend entry point
├── .gitignore
├── package.json
└── README.md

```

---

## ⚙️ Getting Started

Follow these steps to set up and run the application locally.

### **Prerequisites**

Make sure you have the following installed on your machine:

* [Node.js](https://nodejs.org/?utm_source=gemini) (v16.x or higher)
* [npm](https://www.npmjs.com/?utm_source=gemini) or [yarn](https://yarnpkg.com/?utm_source=gemini)
* [MongoDB](https://www.mongodb.com/?utm_source=gemini) (Local instance or MongoDB Atlas connection string)

---

### **1. Clone the Repository**

```bash
git clone [https://github.com/ChethanPutran/Chat-App.git](https://github.com/ChethanPutran/Chat-App.git)
cd Chat-App

```

### **2. Configure Environment Variables**

Create a `.env` file in the `server` directory (and `client` directory if required) with the following key-value pairs:

#### **Server (`server/.env`)**

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/chatapp
JWT_SECRET=your_jwt_secret_key_here
CLIENT_URL=http://localhost:3000

```

#### **Client (`client/.env`)**

```env
REACT_APP_SERVER_URL=http://localhost:5000

```

---

### **3. Install Dependencies & Run**

#### **Setup Server**

```bash
cd server
npm install
npm start

```

*(The server will typically run on `http://localhost:5000`)*

#### **Setup Client**

In a new terminal window:

```bash
cd client
npm install
npm start

```

*(The client application will open at `http://localhost:3000`)*

---

## 🔌 API Endpoints (Overview)

| Method | Endpoint | Description | Auth Required |
| --- | --- | --- | --- |
| `POST` | `/api/auth/register` | Register a new user | ❌ |
| `POST` | `/api/auth/login` | Authenticate user & receive token | ❌ |
| `GET` | `/api/users` | Fetch all available users | ✅ |
| `GET` | `/api/messages/:id` | Fetch message history with a user | ✅ |
| `POST` | `/api/messages/send` | Send a new message | ✅ |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. **Fork** the repository.
2. **Create** a new branch (`git checkout -b feature/AmazingFeature`).
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`).
4. **Push** to the branch (`git push origin feature/AmazingFeature`).
5. Open a **Pull Request**.


---

### 💡 How to Add This to Your Repo

1. In your local repository directory, create or open `README.md`:
   ```bash
   nano README.md
   # or edit with VS Code
   code README.md

```

2. Paste the contents above and save.
3. Commit and push to GitHub:
```bash
git add README.md
git commit -m "docs: add comprehensive README.md"
git push origin main
```
