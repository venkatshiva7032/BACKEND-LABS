# Backend Development Fundamentals — Labs Portfolio

A structured collection of backend engineering lab projects developed as part of the **Backend Development Fundamentals** course. This repository showcases progressive server-side application development using Node.js, Express.js, and SQLite database integration.

---

## 👨‍🎓 Student Details

| Field | Details |
|---|---|
| **Student Name** | V. Venkatshiva |
| **Section** | CSE-GAI-2c |
| **Course** | Backend Development Fundamentals |

---

## 📁 Repository Overview

This mono-repository organizes individual lab assignments into distinct, self-contained directories. Each lab includes its own dependencies, scripts, environment configurations, and documentation.

```text
BACKEND LABS/
├── lab-1/          # Lab 1: Core HTTP & Express.js fundamentals
└── lab-2/          # Lab 2: SQLite database connection & CRUD routes
```

- 📂 **[Lab 1 — Core Fundamentals](./lab-1/)**
- 📂 **[Lab 2 — SQLite Database & CRUD Routes](./lab-2/)**

---

## 🧪 Lab Details

### 🔹 [Lab 1: Backend Development Fundamentals Lab 1](./lab-1/)

Lab 1 introduces the principles of backend engineering and web server architecture. It demonstrates building HTTP servers using native Node.js as well as creating structured routing with Express.js.

#### Key Highlights & Functionality
- **Native HTTP & Express Servers**: Compares native Node.js `http.createServer` with Express application routing.
- **RESTful Endpoints**:
  - `GET /` — Welcome message and root service check.
  - `GET /about` — Returns developer and section metadata in JSON.
  - `GET /time` — Returns the current server timestamp in ISO 8601 format.
  - `404 Handler` — Catches unhandled routes and returns standard JSON error responses.
- **Automated Testing & Deployment**: Integration tests using the native Node.js test runner and live deployment integration.

#### Technologies Used
*(Referenced from [`lab-1/package.json`](./lab-1/package.json))*
- **Runtime Environment:** Node.js (CommonJS)
- **Production Dependencies:**
  - `express` (`^5.3.0`): Web framework for routing and middleware.
- **Development Dependencies:**
  - `playwright` (`^1.64.1`): End-to-end testing and browser automation.
- **Testing:** Native Node.js test runner (`node --test`).

---

### 🔹 [Lab 2: SQLite Database and CRUD Routes](./lab-2/)

Lab 2 expands backend capabilities into persistent data storage. It integrates an SQLite relational database with an Express application, implementing complete CRUD (Create, Read, Update, Delete) operations with parameterization and error handling.

#### Key Highlights & Functionality
- **Database Initialization**: Asynchronous connection lifecycle management using `sqlite` and `sqlite3`, creating the `book` table schema automatically upon server startup.
- **RESTful CRUD Endpoints**:
  - `GET /` — API documentation page listing all routes.
  - `GET /books/` — Retrieves all book records from SQLite.
  - `GET /books/:bookId/` — Retrieves a specific book record by primary key ID.
  - `POST /books/` — Inserts a new book into the database with payload validation.
  - `PUT /books/:bookId/` — Updates an existing book record using SQL `UPDATE`.
  - `DELETE /books/:bookId/` — Removes a book record using SQL `DELETE`.
- **Query Parameterization**: Protects against SQL injection by utilizing prepared and parameterized SQLite queries.

#### Technologies Used
*(Referenced from [`lab-2/package.json`](./lab-2/package.json))*
- **Runtime Environment:** Node.js (CommonJS)
- **Database:** SQLite (`books.db`)
- **Production Dependencies:**
  - `express` (`^5.3.0`): Web framework for REST API routing and JSON parsing middleware.
  - `sqlite` (`^5.1.1`): Promise-based SQLite client wrapper.
  - `sqlite3` (`^5.1.7`): SQLite3 driver engine.
- **Development Dependencies:**
  - `nodemon` (`^3.1.14`): Development utility for live server reloading.

---

## 🚀 Getting Started & Execution Instructions

Each lab is an isolated project with independent dependency definitions. You can install and run each lab separately as detailed below.

### Prerequisites
- **Node.js** (v18.x or later recommended)
- **npm** (v9.x or later)

---

### Running Lab 1

1. **Navigate to the Lab 1 directory:**
   ```bash
   cd lab-1
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the application:**
   ```bash
   npm start
   ```
   The Express server will start on `http://localhost:3000/`.

4. **Run automated tests:**
   ```bash
   npm test
   ```

---

### Running Lab 2

1. **Navigate to the Lab 2 directory:**
   ```bash
   cd lab-2
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the application:**
   - **Production mode:**
     ```bash
     npm start
     ```
   - **Development mode** (with auto-restart via nodemon):
     ```bash
     npm run dev
     ```
   The server will initialize the SQLite database (`books.db`) and start on `http://localhost:3000/`.

---

## 🎯 Conclusion

Across these labs, foundational and intermediate backend engineering competencies were developed and put into practice:
- Transitioning from foundational HTTP server concepts to production-grade Express.js REST APIs.
- Designing predictable JSON APIs following HTTP methods (`GET`, `POST`, `PUT`, `DELETE`) and standard HTTP status codes.
- Managing asynchronous workflows with modern `async`/`await` patterns.
- Integrating relational database persistence using SQLite with parameterized SQL statements.
- Organizing modular, clean, and testable backend projects.

