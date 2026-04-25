# 🌱 Daily Check-in App

A full-stack wellness monitoring application designed to help people stay connected and safe through daily check-ins.

This project allows users to check in daily and assign trusted contacts (monitors) who can ensure their wellbeing.

---

## 🎥 Demo

👉 https://youtube.com/watch?si=UwjtfH6zIyhKirM4&v=2ZK5sO_DsA0&feature=youtu.be

---

## 🚀 Features

### 👤 User Roles
- **Lonely Person**
  - Performs daily check-ins
  - Adds/removes trusted monitors
- **Close Person (Monitor)**
  - Monitors check-in activity of assigned users *(future improvements: alerts & notifications)*

---

### 📊 Dashboard
- Daily check-in button
- Last check-in timestamp
- Role-based behavior
- Secure authentication (token-based)

---

### 👀 Monitor Management
- Add monitor by email
- Validation:
  - Must exist in system
  - Must have correct role
  - Cannot add yourself
- Remove monitors

---

### 🔄 Role Management
- Choose role during registration
- Update role from dashboard *(implemented feature)*

---

### 🔐 Authentication
- Token-based authentication (Django REST Framework)
- Auto-login after registration

---

## 🏗️ Tech Stack

### Backend
- Python 3
- Django 5
- Django REST Framework

### Frontend
- React (TypeScript)
- Axios
- React Router
- React Toastify

### Database
- SQLite (development)

---



daily-checkin-app/
│
├── backend/
│ ├── core/ # Check-in logic
│ ├── monitors/ # Monitor relationships
│ ├── users/ # User profile (roles)
│ ├── config/ # Django settings
│ └── manage.py
│
├── frontend/
│ ├── src/
│ │ ├── pages/
│ │ │ ├── Dashboard.tsx
│ │ │ ├── Monitors.tsx
│ │ │ ├── Login.tsx
│ │ │ └── Register.tsx
│ │ ├── App.tsx
│ │ └── main.tsx
│ └── package.json
│
└── README.md




---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/daily-checkin-app.git
cd daily-checkin-app



### 2. Backend Setup

cd backend
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

pip install -r requirements.txt
python manage.py migrate
python manage.py runserver



### 3. Frontend Setup

cd frontend
npm install
npm run dev



### 📦 requirements.txt

Django==5.0
djangorestframework==3.15.1
django-cors-headers==4.3.1


## 🔌 API Overview
| Endpoint               | Method | Description             |
| ---------------------- | ------ | ----------------------- |
| `/api/register/`       | POST   | Register user with role |
| `/api/api-token-auth/` | POST   | Login and get token     |
| `/api/dashboard/`      | GET    | Get last check-in       |
| `/api/checkin/`        | POST   | Perform check-in        |
| `/api/monitors/`       | GET    | List monitors           |
| `/api/monitors/`       | POST   | Add monitor             |
| `/api/monitors/{id}/`  | DELETE | Remove monitor          |




## 🧠 How It Works

- User registers and selects a role (**Lonely** or **Close Person**)
- **Lonely users:**
  - Check in daily
  - Add trusted monitors
- Monitor relationships are validated by role
- Backend stores:
  - Check-in timestamps
  - User roles
  - Monitor relationships
- Frontend displays real-time data via API calls

---

## 🌟 Example Use Case

- Alice registers as a **Lonely Person**
- She adds Bob (a **Close Person**) as her monitor
- Alice checks in daily
- If she misses a check-in, Bob can follow up

---

## 📈 Future Improvements

- Email/SMS alerts for missed check-ins
- Push notifications
- Role-based dashboards
- Mobile app (React Native)
- Deployment (AWS / Docker)

---

## 🇸🇪 Why This Project Stands Out (For Recruiters)

- Demonstrates full-stack development (**React + Django**)
- Clean separation of concerns (**frontend/backend**)
- Real-world use case (**wellbeing monitoring**)
- Secure authentication & validation logic
- Scalable architecture for future features
- Strong focus on user roles and business logic

---

## 👨‍💻 Author

**Your Name**  
📍 Sweden  
🔗 LinkedIn: [https://linkedin.com/in/yourprofile  ](https://www.linkedin.com/in/khosiyat-sabir-ova-01603377/) 
💻 GitHub: [https://github.com/yourusername](https://github.com/Khosiyat)

## 📁 Project Structure

