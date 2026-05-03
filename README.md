# WorkSync

WorkSync is a project and task management tool built for small teams. You can create projects, assign work to teammates, and track what's getting done — all in one place.

## Features

- User registration and login
- Create and manage multiple projects
- Add team members to projects
- Create tasks, set priorities, assign them to people
- Kanban board with four stages — To Do, In Progress, Review, Done
- Overview dashboard with task stats and recent activity
- Admin users can manage the whole team

## Stack

- **Node.js + Express** for the backend API
- **MySQL** for the database
- **JWT** for authentication
- **HTML/CSS/JS** for the frontend (no build tools needed)
- **Deployed on Railway**

## Local setup

```bash
npm install
```

Create a `.env` file in the root:

```
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=task_team_manager
JWT_SECRET=pick_any_secret
NODE_ENV=development
```

Initialize the database:

```bash
node server/database/setup.js
```

Run the app:

```bash
npm start
```

Open `http://localhost:5000`

## How roles work

When you sign up you pick either **Administrator** or **Team Member**.

- Administrators can create projects, add or remove members, manage all tasks, and see the full user list
- Team Members can see projects they're added to, create tasks, update task status, and comment on tasks

## Deployed at

https://task-team-manager-production-88c7.up.railway.app
