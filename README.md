# Project SI-SW Team 8

A collaborative backend REST API project built with **Express.js**, **Prisma ORM**, and **MySQL**, developed as a group assignment during a software development course. The project follows an **MVC architecture** with separate layers for routing, controllers, helpers, and modules.

---

## Features

- **MVC Architecture** : organized into controllers, helpers, modules, and routes
- **CRUD Endpoints** : Create, Read, Update, and Delete for `User` resource
- **Prisma ORM** : type-safe MySQL database access with schema-defined models
- **Joi Validation** : request body validation with schema enforcement
- **Modular Routing** : centralized route registration via `routes.js`
- **Error Handling** : try/catch on all async routes with HTTP status codes

---

## Tech Stack

| Technology | Description |
|------------|-------------|
| Node.js | JavaScript runtime |
| Express.js | Web framework for the REST API |
| Prisma ORM | Database schema manager and query client |
| MySQL | Relational database |
| Joi | Request schema validation |
| express-joi-validation | Joi validation middleware for Express |

---

## File Structure

```
project-SI-SW-team-8/
├── controllers/
│   └── UserControllers.js   # Request handlers for user routes
├── helpers/                 # Utility/helper functions
├── modules/                 # Reusable modules
├── prisma/
│   └── schema.prisma        # Database schema definition
├── routes.js                # Centralized route registration
├── index.js                 # Express app entry point
├── package.json
└── .gitignore
```

---

## Database Schema

```prisma
model User {
  id             Int    @id @default(autoincrement())
  name           String @unique
  contact        String
  email          String
  incoming_funds String
  cash_out       String
  description    String
}
```

---

## API Endpoints

Base URL: `http://localhost:3000`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Health check |
| GET | `/api/users` | Get user data |
| POST | `/user/create` | Create a new user |
| PATCH | `/user/update` | Update an existing user |
| DELETE | `/user/delete` | Delete a user by name |

---

## Getting Started

### Prerequisites
- Node.js installed
- MySQL database running

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/bellatrijuliana/project-SI-SW-team-8.git
   cd project-SI-SW-team-8
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with your database connection:
   ```env
   DATABASE_URL="mysql://USER:PASSWORD@localhost:3306/DATABASE_NAME"
   ```

4. Run Prisma migration:
   ```bash
   npx prisma migrate dev
   ```

5. Start the server:
   ```bash
   node index.js
   ```

API will be running at `http://localhost:3000`.

---

## Team

This project was built collaboratively as a group assignment — **Team 8**.

---

## What I Learned

- Structuring a backend project with **MVC architecture**
- Registering routes dynamically using a **centralized router**
- Defining and migrating a **Prisma schema** with relational data
- Collaborating on a codebase using **Git and GitHub**
- Building on top of individual practice to create a **team project**

---

*Built as a group project assignment for a Software Development course.*
