# SQL login bypass
## Database schema

```sql
CREATE DATABASE banking_app;

-- Use the database
USE banking_app;

-- Create the `users` table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    fullname VARCHAR(255),
    email VARCHAR(255),
    phone VARCHAR(20),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Insert sample data into `users`
INSERT INTO users (username, password, fullname, email, phone)
VALUES ('admin', 'password123', 'Admin User', 'admin@bank.com', '0771234567');

INSERT INTO users (username, password, fullname, email, phone)
VALUES ('john', 'johnpass', 'John Doe', 'john@example.com', '0779876543');
```

## URL

    http://localhost:4000/login

## request body for login request

```
{
    "username": "admin",
    "password": "password123"
}
```
