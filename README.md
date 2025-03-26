# JWT Kanban Board

## Project Overview

The JWT Kanban Board is a full-stack application designed to manage tasks within an agile team using a Kanban-style board. It includes a secure login page that authenticates users with JSON Web Tokens (JWT) and a main Kanban board page for managing tasks across three columns based on their status.

## Key Features:

- **User Authentication with JWT** (Login/Logout).
- **Persistent session** stored in `localStorage`.
- **Task management** with Kanban board view, allowing tasks to be moved between columns.
- **Protected routes** to ensure the user must be authenticated to access the Kanban board.

## Project Details

- Authentication: Users authenticate through a secure login form, and their session is validated using JWT.
- Kanban Board: The main page displays a list of tasks, allowing users to move tasks between different columns (To Do, In Progress, Done).
- Security: JWT tokens are used to protect the routes and ensure only authenticated users can access the board.

## Installation & Setup

To get started with this project:

Clone this repository to your local machine:

```bash
git clone https://github.com/Anshul1555/JWT-KanbanBoard.git
cd JWT-KanbanBoard
```

1. Install server dependencies:

```bash
cd server
npm install
```

2. Install client dependencies:

```bash
cd ../client
npm install
```

3. Create a .env file for the server with the following content:

```bash
DB_USERNAME=<your-database-username>
DB_PASSWORD=<your-database-password>
JWT_SECRET=<your-jwt-secret-key>
```

4. Start the server:

```bash
cd ../server
npm run dev
```

5. Start the client:

```bash
cd ../client
npm start
```

6. The application will be available at http://localhost:3000.

## Key Features

- **Login Page**: Secure login form where users can enter their username and password.
- **JWT Authentication**: Upon successful login, a JWT token is generated and stored in the browser's `localStorage` for subsequent API requests.
- **Protected Routes**: The Kanban board page is protected, meaning only authenticated users can access it.
- **Session Management**: JWTs are stored securely in `localStorage` and are invalidated upon logout or after a certain inactivity period.
- **Kanban Board**: A visual task board that shows tasks categorized into different columns (To Do, In Progress, Done), where tasks can be moved between columns.

## Deployment

The application is deployed on Render and can be accessed at:

**Live URL**: [Insert your deployed app URL here]

## Technologies Used

- **Backend**: Node.js, Express, PostgreSQL
- **Frontend**: React
- **Authentication**: JSON Web Tokens (JWT)
- **Deployment**: Render
- **Styling**: CSS (Custom styling)

## How to Use

1. **Login**: Enter your username and password on the login page.
2. **Access Kanban Board**: After successful login, you'll be redirected to the Kanban board where you can view and manage tasks.
3. **Logout**: Click the logout button to log out, which will remove the JWT from `localStorage` and redirect you back to the login page.
