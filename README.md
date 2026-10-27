# StaffSync - Modern Human Resource Management Solution

StaffSync is a comprehensive web-based HR management application built using the **MERN Stack** (MongoDB, Express.js, React.js, Node.js). It streamlines and automates HR processes within an organization with role-based access for **HR**, **Managers**, and **Employees**.

## Features

### HR
- Add, edit, and delete employees
- Post and delete company announcements
- View all leave requests
- View attendance records

### Manager
- View team leave requests (same department)
- Approve or reject leaves
- Create and assign training programs

### Employee
- Apply for leave and track leave status
- Mark daily attendance
- View company announcements
- Update personal profile

### General
- JWT-based authentication
- Password hashing with bcrypt
- Role-based protected routes
- Responsive UI with Bootstrap

## Tech Stack

| Layer | Technologies |
|-------|--------------|
| Frontend | React (Vite), React Router, Axios, Bootstrap, Context API |
| Backend | Node.js, Express.js |
| Database | MongoDB (Mongoose) |
| Auth | JSON Web Token (JWT), bcryptjs |

## Project Structure

```
staffsync/
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── server.js
│   └── .env.example
├── frontend/
│   ├── src/
│   └── package.json
└── README.md
```

## Database Models

- **User**: name, email, password, role (hr / manager / employee), department
- **Leave**: employee, fromDate, toDate, reason, status (pending / approved / rejected)
- **Attendance**: employee, date, status
- **Announcement**: title, message, createdBy, date
- **Training**: title, description, manager, employees

## Getting Started

### Prerequisites
- Node.js (v18 or above)
- MongoDB Atlas account or local MongoDB

### 1. Clone the repository
```bash
git clone https://github.com/gaurii183/staffsync.git
cd staffsync
```

### 2. Setup Backend
```bash
cd backend
npm install
```

Create a `.env` file in the `backend` folder (see `.env.example`):
```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Start the server:
```bash
npm start
```
Backend runs on `http://localhost:5000`

### 3. Setup Frontend
Open a new terminal:
```bash
cd frontend
npm install
npm run dev
```
Frontend runs on `http://localhost:5173`

## Usage

1. Open `http://localhost:5173`
2. Register accounts for each role (HR, Manager, Employee)
3. Use the same department for Manager and Employee so the manager can see the team's leave requests
4. Log in and explore the role-specific dashboard

## Screenshots

_Add screenshots of the Login page, HR Dashboard, Manager Dashboard, and Employee Dashboard here._

## Future Improvements

- Payroll management
- Email notifications for leave status
- Performance reviews
- Attendance reports and analytics

## Author

**YOUR NAME**
GitHub: [@gaurii183](https://github.com/gaurii183)

## License

This project is for educational purposes.
