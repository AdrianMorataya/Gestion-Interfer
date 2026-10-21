# Gestion Interfer API

A RESTful API built with Node.js, Express and MongoDB to support authentication, administration and company management.

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express-404040?style=flat-square&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Swagger-85A548?style=flat-square&logo=swagger&logoColor=white" alt="Swagger" />
</p>

---

## Overview

**Gestion Interfer API** is a backend application designed to centralize business-related operations through a structured REST API.

The project follows a modular architecture, separating authentication, administration, company management, database configuration and request validation.

## Features

- **Authentication:** User registration and login endpoints.
- **Admin management:** Dedicated routes for administrative operations.
- **Company management:** A separate module for company-related operations.
- **MongoDB integration:** Database connectivity using Mongoose.
- **Input validation:** Request validation using Express Validator.
- **Security middleware:** Helmet, rate limiting and Argon2 password hashing support.
- **File uploads:** Profile picture upload handling with Multer.
- **API documentation:** Swagger UI and OpenAPI documentation.
- **Data processing:** Excel spreadsheet support through XLSX.
- **Logging:** HTTP request logging with Morgan.

## Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| Express.js | REST API framework |
| MongoDB | Database |
| Mongoose | Database modeling and connectivity |
| JSON Web Token | Token-based authentication support |
| Argon2 | Password hashing |
| Swagger | API documentation |
| Multer | File upload handling |
| Helmet | HTTP security headers |
| Express Validator | Request validation |

## Project Structure

```text
Gestion-Interfer/
├── configs/
│   ├── mongo.js
│   ├── server.js
│   └── swagger.js
├── public/
│   └── uploads/
│       └── profile-pictures/
├── reports/
├── src/
│   ├── auth/
│   ├── admin/
│   ├── company/
│   └── middlewares/
├── .env
├── .gitignore
├── index.js
├── package.json
└── README.md
```

## Getting Started

### Prerequisites

Make sure you have installed:

- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/)
- npm, included with Node.js

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/AdrianMorataya/Gestion-Interfer.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Gestion-Interfer
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

### Environment Variables

Create a `.env` file in the project root and configure the variables required by the application.

```env
PORT=3000
URI_MONGO=mongodb://127.0.0.1:27017/gestion_interfer
```

Use your actual database connection string and the configuration required by your implementation. Keep credentials, secrets and production environment variables out of version control.

### Run the Application

Start the server:

```bash
npm start
```

Start the development server with automatic restarts:

```bash
npm run dev
```

## API Documentation

The application includes Swagger UI for exploring and testing the documented API endpoints.

Once the server is running, visit:

```text
http://localhost:3000/gestorInterfer/v1/api-docs
```

Replace `3000` with the port configured in your `.env` file.

## API Modules

| Base path | Description |
|---|---|
| `/gestorInterfer/v1/auth` | Registration and login |
| `/gestorInterfer/v1/admin` | Administrative endpoints |
| `/gestorInterfer/v1/company` | Company management endpoints |
| `/gestorInterfer/v1/api-docs` | Swagger API documentation |

## Security

The project incorporates several security-related components, including password hashing support, request validation, rate limiting and HTTP security headers.

For production deployments, configure CORS with trusted origins, protect sensitive environment variables, and ensure authentication and authorization are correctly enforced across protected endpoints.

## License

This project includes an ISC license. See the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <sub>Developed by <a href="https://github.com/AdrianMorataya">Adrian Morataya</a></sub>
</p>
