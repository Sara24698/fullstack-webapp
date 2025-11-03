# 💻 Fullstack WebApp

**Fullstack WebApp** is a complete web application built with **Node.js + Express** on the backend and **React** on the frontend.  
It provides a foundation for creating a system that manages **users, friends, and presents 🎁**, including an API server, SQL database connection, and a modern, modular user interface.

This project serves as a clean and practical example of a **fullstack architecture**, with each layer clearly separated to improve scalability, maintainability, and collaboration.

---

## 🧭 Overview

The application is organized into **three main layers**:

1. 🖥️ **Frontend (`frontend/`)**  
   The main **React interface** where users can register, manage friends, and interact with presents.  
   It includes reusable components, global variables (defined in `Globals.js`), and custom styles.

2. ⚙️ **Backend (`Backend/`)**  
   A **RESTful API** built with **Express**, handling all requests from the frontend, connecting to the SQL database, and returning JSON responses.  
   It has separate route modules for users, friends, and presents, plus a lightweight API key management system.

3. 🗄️ **Database (`Base_datos.sql`)**  
   A SQL script that defines the database schema, compatible with **MySQL** or **MariaDB**.  
   It includes the main tables and relationships for users, friends, and presents.

Additionally, there is an optional folder `front_antdesign/`, which provides an **alternative frontend version** using **Ant Design**, a professional UI library for a more stylized or corporate look.

---

## 🏗️ Project Structure

- **fullstack-webapp/**
  - **Backend/**
    - `app.js` — Main Express server
    - `database.js` — SQL connection configuration
    - `activeApiKeys.js` — API key management
    - **Routers/**
      - `Users.js` — User endpoints
      - `Friends.js` — Friends endpoints
      - `Presents.js` — Presents endpoints
  - **frontend/**
    - `public/`
    - **src/**
      - **Components/** — Reusable React components
      - `App.js` — Root component
      - `Globals.js` — Global configuration
      - `App.css` — Base styles
      - `index.js` — Entry point
  - **front_antdesign/** — Optional Ant Design–based frontend
  - `Base_datos.sql` — SQL database schema
  - `.gitignore`
 
## Configure the database

Import the SQL file into your local database:
`mysql -u your_user -p < Base_datos.sql`

Then, update the connection settings in Backend/database.js
`const connection = mysql.createConnection({
  host: 'localhost',
  user: 'your_user',
  password: 'your_password',
  database: 'your_database'
});
`

## 🧩 Internal Structure and Functionality

### 🔹 Backend

The backend is built with **Express** and exposes modular routes located in `Backend/Routers/`:

| **Route** | **Description** |
|------------|-----------------|
| `/users`   | Handles user creation, login, and management |
| `/friends` | Manages friendships and relationships |
| `/presents`| Creates and retrieves presents data |

Additional backend files:

- `activeApiKeys.js` — Manages active API keys for authentication or session validation.  
- `database.js` — Handles the SQL connection setup.

---

### 🔹 Frontend

The **React** client provides a clean, component-based structure:

- `src/Components/` — Contains reusable UI components.  
- `Globals.js` — Defines global constants such as the backend URL.  
- `App.js` — Structures the main layout.  
- `App.css` — Defines global styles.  

The application communicates with the backend API using **fetch** or **Axios** to retrieve and manipulate data in real time.

---

### 🔹 Database

The database schema (`Base_datos.sql`) defines the key relationships:

| **Table** | **Purpose** |
|------------|-------------|
| `Users`    | Stores user data |
| `Friends`  | Defines user friendships |
| `Presents` | Contains presents assigned to users |

## 💡 Customization

- Add or edit API routes in `Backend/Routers/`.  
- Update frontend API URLs in `Globals.js`.  
- Use the `front_antdesign/` folder if you prefer to work with **Ant Design** components.


