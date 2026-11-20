# DocDirect – Doctor Appointment Booking Platform

<p align="center">
  <b>A Full-Stack Healthcare Appointment Management System</b>
</p>

<p align="center">
  A web-based platform that connects patients with doctors, simplifies appointment booking, and provides dedicated dashboards for administrators and doctors.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-Backend-339933?logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-API-000000?logo=express" />
  <img src="https://img.shields.io/badge/MongoDB-Database-47A248?logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/TailwindCSS-Styling-06B6D4?logo=tailwindcss&logoColor=white" />
</p>

---

## Overview

**DocDirect** is a full-stack doctor appointment booking platform developed using the MERN stack. It provides a centralized system where patients can explore doctors, view their profiles, and book appointments online.

The platform includes three separate interfaces:

- **Patient Panel:** Browse doctors, manage personal profiles, and book or track appointments.
- **Admin Panel:** Manage doctors, monitor appointments, and access dashboard statistics.
- **Doctor Panel:** View appointments, manage appointment availability, and maintain doctor profiles.

The application integrates MongoDB for data storage, Cloudinary for image management, and online payment gateway integrations.

## Features

### Patient Panel
- User registration and login.
- Browse available doctors.
- Search doctors by medical speciality.
- View doctor profiles and appointment details.
- Book doctor appointments.
- Manage personal profile information.
- View and manage booked appointments.
- Online payment integration.

### Admin Panel
- Admin authentication.
- Dashboard with doctors, patients, and appointment statistics.
- Add new doctors.
- View and manage doctor records.
- View all patient appointments.
- Cancel appointments.
- Upload and manage doctor profile images.

### Doctor Panel
- Doctor authentication.
- Doctor dashboard.
- View scheduled appointments.
- Manage appointment-related information.
- Maintain doctor profile details.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite |
| Styling | Tailwind CSS |
| Routing | React Router DOM |
| API Integration | Axios |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcrypt |
| Image Storage | Cloudinary |
| Payment Integration | Razorpay, Stripe |
| Notifications | React Toastify |

## Project Structure

```text
docdirect/
│
├── admin/                  # Admin and Doctor Dashboard
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   └── App.jsx
│   └── package.json
│
├── backend/                # Express Backend
│   ├── config/             # Database and Cloudinary setup
│   ├── controllers/        # Application business logic
│   ├── middlewares/        # Authentication middleware
│   ├── models/             # MongoDB models
│   ├── routes/             # API routes
│   ├── server.js
│   └── package.json
│
├── frontend/               # Patient-facing Application
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
└── README.md
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Shantnupakira2811/docdirect.git
cd docdirect
```

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

### 3. Configure Environment Variables

Create a `.env` file inside the `backend` directory.

```env
PORT=4000

MONGODB_URI=your_mongodb_connection_string

CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key

JWT_SECRET=your_jwt_secret

ADMIN_EMAIL=your_admin_email
ADMIN_PASSWORD=your_admin_password

RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret

STRIPE_SECRET_KEY=your_stripe_secret_key
```

Add the required environment variables according to the integrations enabled in your application.

**Important:** Never upload your `.env` file or expose API keys and database credentials publicly.

### 4. Start the Backend Server

```bash
npm run server
```

The backend server runs on:

```text
http://localhost:4000
```

### 5. Install and Run the Patient Frontend

Open a new terminal:

```bash
cd frontend
npm install
npm run dev
```

### 6. Install and Run the Admin Panel

Open another terminal:

```bash
cd admin
npm install
npm run dev
```

The frontend and admin panel will display their respective local development URLs in the terminal.

## Application Architecture

```text
             PATIENT
                |
                v
       React Patient Frontend
                |
                v
          Axios Requests
                |
                v
       Node.js + Express API
                |
          Authentication
                |
                v
           Controllers
                |
                v
          Mongoose Models
                |
                v
             MongoDB

       ADMIN / DOCTOR
                |
                v
         React Admin Panel
                |
                v
          Express API
```

External integrations:
- Cloudinary – Image storage and management.
- Razorpay / Stripe – Payment processing.

## Key Concepts Implemented

- **REST API:** Communication between frontend and backend.
- **JWT Authentication:** Token-based authentication.
- **Password Hashing:** Secure password storage using bcrypt.
- **MongoDB:** Database management using Mongoose.
- **Role-based Interfaces:** Separate patient, admin, and doctor dashboards.
- **Third-party Integrations:** Cloudinary and payment gateway services.
- **React Context API:** Shared application state management.

## Future Enhancements

- Real-time appointment notifications.
- Video consultation functionality.
- Patient medical history management.
- Doctor availability calendar.
- Automated appointment reminders.
- Improved analytics and reporting.

## Author

**Shantnu Pakira**

- GitHub: [@Shantnupakira2811](https://github.com/Shantnupakira2811)
- Project Repository: [DocDirect](https://github.com/Shantnupakira2811/docdirect)

---

<p align="center">
  <b>DocDirect – Making Healthcare Appointments Simpler.</b>
</p>
