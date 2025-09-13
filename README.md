# Lab Authentication API

A simple Node.js + Express + MySQL API for Lab 3 that implements user signup, login, logout (token revocation), and a protected profile endpoint using JWT.

## Overview
- **Language:** Node.js  
- **Framework:** Express  
- **Database:** MySQL  
- **Auth:** JWT (jsonwebtoken) + bcrypt (bcryptjs)  
- **Token revocation:** stored `jti` in `revoked_tokens` table  


## How to Run (Quick)

1. **Install dependencies:**

```bash
npm install express cors dotenv mysql2 bcryptjs jsonwebtoken uuid
npm install --save-dev nodemon

## API Endpoints

| Method | Endpoint           | Description                       |
|------- | ----------------- | --------------------------------- |
| GET    | `/api/health`      | Health check (no auth required)   |
| POST   | `/api/auth/signup` | Register a new user               |
| POST   | `/api/auth/login`  | Login and receive JWT token       |
| POST   | `/api/auth/logout` | Revoke token (requires token)     |
| GET    | `/api/profile`     | Get current user (requires token) |
