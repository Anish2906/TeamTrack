
🚀 Employee Management System (EMS)

A React app bootstrapped with Vite and styled using Tailwind CSS. EMS showcases role‑based authentication (Admin & Employee), task assignment & tracking, and a lightweight Local Storage data layer.

🌟 Features

🔑 Authentication

Separate login flows for Admin and Employee.

Simple credential check stored in Local Storage (demo‑only).

📝 Task Management

Admin: Create tasks, set priority, due date, and track progress.

Employee: Accept, reject, or update status (In Progress, Completed).

⚙️ Local Storage Backend

Uses browser localStorage for persistence (no external DB).

Seed data for quick start; add more users any time.

💎 UI/UX

Responsive, mobile‑first layout.

Clean, utility‑first styling with Tailwind.

🛠️ Tech Stack

React — Component‑based UI.

Vite — Fast dev server & builds.

Tailwind CSS — Utility‑first styling.

JavaScript (ES6+) — App logic.

Local Storage — Data persistence.

📦 Project Structure (example)

ems/
├─ src/
│  ├─ components/
│  │  ├─ Auth/
│  │  ├─ Tasks/
│  │  └─ UI/
│  ├─ pages/
│  ├─ hooks/
│  ├─ utils/
│  ├─ data/             
│  ├─ App.jsx
│  └─ main.jsx
├─ public/
├─ index.html
├─ tailwind.config.js
├─ postcss.config.js
├─ package.json
└─ README.md

🔐 Demo Credentials

Quick start with pre‑seeded users. You can add more employees with unique usernames.

Admin

Username: admin@me.com

Password: 123

Employee (example)

Username: employee2@example.com

Password: 123

⚙️ Installation & Setup

Clone the repository

git clone 
cd ems

Install dependencies

npm install

Run the dev server

npm run dev

Open http://localhost:5173 in your browser.

🚪 Usage at a Glance

Login as Admin to create/assign tasks.

Switch to an Employee account to accept/reject and update task status.

All data (users, tasks, session) is stored in localStorage.

🧱 Data Model (Local Storage)

Keys may vary by implementation, but a typical shape looks like this:

{
  "ems_users": [
    { "id": "u1", "role": "admin", "email": "admin@me.com", "password": "123" },
    { "id": "u2", "role": "employee", "email": "employee2@example.com", "password": "123" }
  ],
  "ems_tasks": [
    {
      "id": "t1",
      "title": "Create landing page",
      "details": "Hero + CTA + responsive nav",
      "priority": "high",
      "dueDate": "2025-08-31",
      "assigneeId": "u2",
      "status": "assigned" // assigned | accepted | in-progress | completed | rejected
    }
  ],
  "ems_session": { "userId": "u1" }
}

🧪 Available Scripts

npm run dev — Start development server.

npm run build — Production build.

npm run preview — Preview built app.

🔧 Configuration

Tailwind is preconfigured via tailwind.config.js and postcss.config.js.

Add environment‑specific values (if needed) via Vite env files: .env, .env.development, etc.

Since EMS uses Local Storage, no secrets are required for the demo.

🔒 Security Note

This project is for demonstration. Local Storage credentials are not secure. For production:

Replace Local Storage with a real backend (API + DB).

Hash passwords, use proper auth (JWT/OAuth), and role/permission checks on the server.

Add input validation & rate limiting.

🗺️ Roadmap (Nice‑to‑Have)

Drag‑and‑drop task board (Kanban).

Filters & search (status, assignee, due date).

Comments & attachments on tasks.

Notifications/toasts.

Persistence via IndexedDB or real API.

🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a PR.

📄 License

This project is open‑sourced under the MIT License (see LICENSE).

🎯 Goal

EMS demonstrates my ability to:

Build responsive, functional front‑end apps.

Implement simple role‑based access (Admin & Employee).

Manage and track tasks using a Local Storage data layer.

Enjoy using EMS! 🚀
