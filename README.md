# Railway Express + PostgreSQL Template

A simple Node.js Express app with PostgreSQL, ready to deploy on Railway.

## Features
- REST API with Express.js
- PostgreSQL database integration
- Auto-deployable on Railway
- Environment variable configuration

## Setup on Railway
1. Click "Deploy on Railway" (add button link after publishing).
2. Railway will provision a PostgreSQL database and set `DATABASE_URL`.
3. Run the following SQL in the Railway database query editor to set up tables:
   ```sql
   CREATE TABLE users (
     id SERIAL PRIMARY KEY,
     name VARCHAR(100),
     email VARCHAR(100) UNIQUE
   );
   INSERT INTO users (name, email) VALUES ('Test User', 'test@example.com');