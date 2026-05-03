# Assignment: Team Task Manager (Full-Stack)

**Project Name:** WorkSync  
**Live URL:** https://task-team-manager-production-88c7.up.railway.app

This repository is a complete solution for the Full-Stack Team Task Manager assignment. It provides a platform where users can create projects, assign tasks, and track overall progress through a role-based access system.

## 🚀 Key Features

- **Authentication (Signup/Login):** Implemented secure user registration and login endpoints utilizing JSON Web Tokens (JWT).
- **Project & Team Management:** Functionality to spin up new projects and seamlessly invite team members to collaborate.
- **Task Creation, Assignment & Tracking:** Users can log tasks, assign them to teammates, and drag them across different statuses using a Kanban view.
- **Dashboard:** A central overview that calculates total tasks, tracks status distributions, and highlights overdue assignments.

## ⚙️ Requirements Addressed

- **REST APIs + Database (SQL):** The backend is powered by Node.js and Express, providing standard REST APIs. Data is securely managed and queried using a **MySQL** database.
- **Proper Validations & Relationships:** 
  - All incoming API requests are validated.
  - The SQL schema enforces relational integrity between users, projects, and tasks using foreign keys.
- **Role-Based Access Control:** 
  - Implemented `Admin` and `Member` roles.
  - Middleware enforces that only Admins can create projects and manage users, while Members can interact with tasks within their assigned projects.

## 🌐 Deployment (Mandatory)

The application has been successfully deployed and is fully functional on **Railway**. It uses a Railway-hosted Node environment connected to a Railway-provisioned MySQL database instance.

---

### Local Setup Instructions

To run this assignment locally on your machine:

1. Clone the repo and install the required packages: `npm install`
2. Create a `.env` configuration file in the root directory:
   ```env
   DB_HOST=localhost
   DB_PORT=3306
   DB_USER=root
   DB_PASSWORD=your_mysql_password
   DB_NAME=task_team_manager
   JWT_SECRET=any_secret_string
   NODE_ENV=development
   ```
3. Run the automated database setup script: `node server/database/setup.js`
4. Start the application: `npm start`
5. Access the app at `http://localhost:5000`
