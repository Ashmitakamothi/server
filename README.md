# Ashmita Software Solutions - Portal

A comprehensive project management and service request portal designed for seamless collaboration between Admins, Employees, and Clients.

## ✨ Tech Stack

### Frontend
- **Framework**: React 19 (Vite)
- **Routing**: React Router Dom 7
- **State & Data**: Axios for API communication
- **Icons**: Lucide React
- **Styling**: Vanilla CSS with modern Glassmorphism aesthetics

### Backend
- **Runtime**: Node.js
- **Framework**: Express 5
- **Database**: MongoDB (Mongoose 8)
- **Authentication**: JWT (JSON Web Tokens) & BcryptJS for hashing
- **Environment**: TypeScript (server-side)

---


---

## 🚀 Setup Instructions

### 1. Prerequisites
- Node.js (v18+)
- MongoDB (Local or Atlas)

### 2. Database Setup
Create a `.env` file in the `server` directory with the following variables:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
ADMIN_EMAIL=admin@ashmita.com
ADMIN_PASSWORD=admin123
```

### 3. Server Installation
```bash
cd server
npm install
# Seed the initial admin user
npm run seed
# Start the development server
npm run dev
```

### 4. Client Installation
Create a `.env` file in the `client` directory:
```env
VITE_API_URL=http://localhost:5000
```

```bash
cd client
npm install
npm run dev
```

---

## 🔑 Test Login Credentials

| Role | Email | Password |
| :--- | :--- | :--- |
| **Admin** | `admin@ashmita.com` | `admin123` |
| **Employee** | *Create via Admin Panel* | *As assigned* |
| **Client** | *Create via Admin Panel* | *As assigned* |

> [!NOTE]
> Use the Admin account to create Employee and Client users. Once created, they can log in to access their respective portals.

---

## 🛠️ Deployment

### Server (Vercel)
The server is configured to work with Vercel serverless functions. Ensure `connectDB()` is called in `app.ts` to maintain database connectivity.

### Client (Vercel)
The client includes a `vercel.json` for SPA routing.
```json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/index.html" }
  ]
}
```
