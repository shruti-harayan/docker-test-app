# Docker + Node.js + MongoDB CRUD Application

A beginner-friendly project demonstrating how to containerize a Node.js application using Docker Compose and connect it with MongoDB.

This project allows users to register through a simple HTML form, stores the data in MongoDB, and retrieves all users through a REST API.

---

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongo Express
- Docker
- Docker Compose
- HTML
- CSS

---

## Project Workflow

```text
User
   │
   ▼
HTML Registration Form
   │
   ▼
Express Server (Node.js)
   │
   ▼
MongoDB Driver
   │
   ▼
MongoDB Docker Container
   │
   ▼
Mongo Express (Database UI)
```

---

## Features

- User Registration Form
- Store user information in MongoDB
- Retrieve all users using REST API
- Mongo Express dashboard to view database records
- Dockerized MongoDB and Mongo Express
- Docker Compose for multi-container management

---

## Project Structure

```
docker-test-app/
│
├── public/
│   ├── index.html
│   └── style.css
│
├── server.js
├── Dockerfile
├── compose.yaml
├── package.json
├── package-lock.json
└── README.md
```

---

# Docker Containers

This project runs two containers using Docker Compose.

| Container | Purpose |
|-----------|----------|
| MongoDB | Stores application data |
| Mongo Express | Web interface to manage MongoDB |

Start both containers

```bash
docker compose up
```

Stop containers

```bash
docker compose down
```

---

# REST API

## Add User

**POST**

```
/addUser
```

Form Fields

| Field | Type |
|--------|------|
| email | String |
| username | String |
| password | String |

---

## Get All Users

**GET**

```
/getUsers
```

Example Response

```json
[
  {
    "_id": "...",
    "email": "shruti@gmail.com",
    "username": "shruti",
    "password": "pass"
  }
]
```

---

# Application Screenshots

## 1. Registration Form

The frontend allows users to submit their details.

<img width="895" height="507" alt="Screenshot 2026-07-17 134804" src="https://github.com/user-attachments/assets/00383c67-f6f7-4202-b31f-8efbb5760d85" />


```
screenshots/home.png
```

---

## 2. Mongo Express Dashboard

Successfully inserted users into MongoDB.

<img width="948" height="505" alt="Screenshot 2026-07-17 134836" src="https://github.com/user-attachments/assets/0aeda2d6-17a1-4cd5-8871-7c0441d50784" />


```
screenshots/mongo-express.png
```

---

## 3. REST API Response

Retrieving all users using the GET endpoint.

<img width="441" height="236" alt="Screenshot 2026-07-17 134855" src="https://github.com/user-attachments/assets/3309f602-4263-4b23-a9ce-42d5f6715ab2" />


```
screenshots/get-users.png
```

---

## 4. Server Logs

Node.js server successfully connected to MongoDB and inserted data.

<img width="949" height="500" alt="Screenshot 2026-07-17 134959" src="https://github.com/user-attachments/assets/f5f5628b-cb07-4746-b6f1-dad18ff1c4c9" />


```
screenshots/server-log.png
```

---

# Docker Commands Used

Build containers

```bash
docker compose up
```

Run in background

```bash
docker compose up -d
```

Stop containers

```bash
docker compose down
```

View running containers

```bash
docker ps
```

View logs

```bash
docker compose logs
```

---

# What I Learned

During this project I learned how to:

- Build a Node.js backend using Express.
- Connect Node.js with MongoDB using the MongoDB Driver.
- Create a Dockerfile for a Node.js application.
- Use Docker Compose to manage multiple containers.
- Configure MongoDB and Mongo Express using environment variables.
- Expose and map container ports.
- Understand Docker networking between containers.
- Use Mongo Express to inspect database records.
- Build simple REST APIs using GET and POST.
- Handle HTML form submissions with Express.
- Access applications using GitHub Codespaces Port Forwarding.
- Debug Docker-related issues such as:
  - Port conflicts
  - Container startup failures
  - MongoDB connection errors
  - Docker Compose configuration issues

---

# Challenges Faced

While building this project, I encountered several real-world issues:

- MongoDB connection refused (`ECONNREFUSED`)
- Docker Compose configuration not found
- Incorrect YAML formatting
- Port `27017` already in use
- Difference between localhost on Windows and GitHub Codespaces
- Container networking issues
- Understanding forwarded ports in GitHub Codespaces

Resolving these problems helped me gain a better understanding of Docker and backend development.

---

# Future Improvements

- Password hashing using bcrypt
- Input validation
- Error handling middleware
- Environment variables using `.env`
- Docker volumes for persistent MongoDB storage
- User authentication
- JWT implementation
- Deploy using Docker on a cloud platform

---

# Author

**Shruti Harayan**

```

![Server Logs](screenshots/server-log.png)
```
