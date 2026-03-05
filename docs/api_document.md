# API Documentation

This document provides a detailed overview of the available API endpoints for the User Management System (UMS).

## Authentication Modules

### Register User
- **URL:** `/auth/register`
- **Method:** `POST`
- **Body:**
  ```json
  {
    "userName": "john_doe",
    "email": "john@example.com",
    "password": "securepassword123"
  }
  ```

### Login User
- **URL:** `/auth/login`
- **Method:** `POST`
- **Body:**
  ```json
  {
    "email": "john@example.com",
    "password": "securepassword123"
  }
  ```
- **Response:** Returns a JWT token.

## User Modules

### Get All Users
- **URL:** `/user`
- **Method:** `GET`
- **Headers:** `token: <JWT_TOKEN>`

### Delete User
- **URL:** `/user/:id`
- **Method:** `DELETE`
- **Headers:** `token: <JWT_TOKEN>`

## Blog Modules

### Create Blog
- **URL:** `/blog`
- **Method:** `POST`
- **Headers:** `token: <JWT_TOKEN>`
- **Body:**
  ```json
  {
    "title": "My First Blog",
    "content": "Hello world!"
  }
  ```

### Get Blog Details
- **URL:** `/blog/:id`
- **Method:** `GET`
