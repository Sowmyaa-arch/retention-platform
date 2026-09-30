# Employee Leave Management System (ELMS)

A full-stack **Employee Leave Management System** built with React, Node.js, Express, and MongoDB. The system provides separate portals for Employees, Managers, and Admins to manage leave requests, approvals, employee data, and analytics.

##  Features

* JWT Authentication** with role-based access control
* Employee Portal** – Apply for leave, view leave history, and check leave balance
* Manager Portal** – Review, approve, and reject leave requests
* Admin Portal** – Manage employees, managers, and leave records
* Analytics Dashboard** – View leave trends, departments, and request statuses
* Responsive UI** built with Tailwind CSS
* RESTful APIs** for authentication, users, and leave management

## 🛠️ Tech Stack

### Frontend

* React 19
* Tailwind CSS
* React Router
* Recharts
* Vite

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT Authentication

### Tools

* Git & GitHub
* Postman
* MongoDB Atlas

##  Project Structure

```text
Leave-management-system/
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── server.js
│   └── seed.js
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── layouts/
│   │   ├── pages/
│   │   ├── routes/
│   │   └── services/
│   └── App.jsx
│
└── ELMS.postman_collection.json
```

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Sowmyaa-arch/Leave-management-system.git
cd Leave-management-system
```

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

### 3. Install Frontend Dependencies

```bash
cd ../frontend
npm install
```

### 4. Configure Environment Variables

Create a `.env` file inside the `backend` folder:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

Create a `.env` file inside the `frontend` folder:

```env
VITE_API_URL=http://localhost:5000/api
```

### 5. Seed the Database

```bash
cd backend
npm run seed
```

### 6. Run the Application

Start the backend:

```bash
cd backend
npm run dev
```

Start the frontend in another terminal:

```bash
cd frontend
npm run dev
```

The application will be available at:

```text
Frontend: http://localhost:3000
Backend:  http://localhost:5000
```

##  API Overview

| Method | Endpoint                  | Access   | Purpose               |
| ------ | ------------------------- | -------- | --------------------- |
| POST   | `/api/auth/register`      | Public   | Register user         |
| POST   | `/api/auth/login`         | Public   | User login            |
| GET    | `/api/auth/profile`       | Private  | Get profile           |
| POST   | `/api/leaves/apply`       | Employee | Apply for leave       |
| GET    | `/api/leaves/my`          | Employee | View own leaves       |
| GET    | `/api/leaves/pending`     | Manager  | View pending requests |
| PUT    | `/api/leaves/approve/:id` | Manager  | Approve leave         |
| PUT    | `/api/leaves/reject/:id`  | Manager  | Reject leave          |
| GET    | `/api/leaves/all`         | Admin    | View all leaves       |

##  API Testing

The project includes a Postman collection:

```text
ELMS.postman_collection.json
```

Import the collection into **Postman** to test the available REST APIs.

##  Security

* JWT-based authentication
* Role-based authorization
* Protected API routes
* Environment variables for sensitive configuration
* Secure access separation between Employee, Manager, and Admin roles

##  Future Improvements

* Email notifications for leave approvals/rejections
* Calendar integration
* Advanced employee reports
* Attendance management
* Automated leave balance calculations

## 📄 License

This project is licensed under the **MIT License**.
