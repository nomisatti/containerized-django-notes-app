# 🐳 Dockerized Django Notes App (Three-Tier Setup)

This project demonstrates how to **containerize and run a Django application** using a **three-tier architecture** with Docker Compose.

> ⚠️ Note: The core Django Notes application was sourced from an existing project.
> The primary focus of this repository is **Dockerization, service orchestration, and deployment setup**.

---

## 📌 Project Goal

The goal of this project is to:

* Containerize a Django application
* Configure a multi-container environment
* Use Nginx as a reverse proxy
* Connect Django with MySQL in a Docker network
* Simulate a production-like setup using Docker Compose

---

## 🏗️ Architecture

```id="arch1"
Client (Browser)
        ↓
     Nginx (Reverse Proxy)
        ↓
     Django App
        ↓
     MySQL Database
```

---

## ⚙️ Tech Stack

* Docker
* Docker Compose
* Nginx (Reverse Proxy)
* Django (App Layer)
* MySQL (Database)


---

## 🐳 Services Overview

| Service   | Description                   |
| --------- | ----------------------------- |
| **web**   | Django application container  |
| **db**    | MySQL database container      |
| **nginx** | Reverse proxy serving the app |

---

## 🔑 Environment Variables

```id="env1"
DB_NAME=test_db
DB_USER=root
DB_PASSWORD=root
DB_PORT=3306
DB_HOST=db_cont
```

---

## ▶️ Run the Project

### 1. Clone repo

```id="run1"
git clone [https://github.com/nomisatti/containerized-django-notes-app.git]
cd django-notes-app
```

### 2. Start containers

```id="run2"
docker-compose up --build
```

### 3. Access app

```id="run3"
http://localhost
```

---

## 🧪 Useful Commands

```id="cmd1"
# Stop containers
docker-compose down

# View logs
docker-compose logs -f

# Rebuild
docker-compose up --build
```

---

## 🚀 Key DevOps Concepts Demonstrated

* Multi-container application setup
* Service communication via Docker network
* Reverse proxy configuration using Nginx
* Environment-based configuration using `.env`
* Persistent database setup with MySQL
* Container orchestration with Docker Compose

---

## 📈 Learning Outcome

Through this project, I gained hands-on experience in:

* Structuring real-world Docker setups
* Debugging container networking issues
* Managing service dependencies
* Running production-like environments locally

---

## 🔮 Future Improvements

* Add CI/CD pipeline (GitHub Actions)
* Deploy to cloud (AWS / DigitalOcean)
* Add HTTPS (Nginx + SSL)
* Kubernetes deployment

---

## 🙌 Credits

* Original Django Notes App: *[https://github.com/LondheShubham153/django-notes-app]*

---

## 👨‍💻 Author

Muhammad Nouman Atiq
