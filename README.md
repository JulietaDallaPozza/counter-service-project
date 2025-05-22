<<<<<<< HEAD
# counter-service-project
Python web service that counts POST requests and returns the count on GET requests
=======
# 🧮 Counter-Service – Python Web App with CI/CD

This repository contains a Python service called **`counter-service`**, developed as part of a DevOps-focused project.

The service exposes an HTTP endpoint that:

- Serves a **web page** and **API** with a counter.
- **Increments** the counter on every `POST` request.
- **Returns** the current counter value on every `GET` request.

---

## 🧱 Tech Stack

- **Python** (Flask or FastAPI)
- **Docker** & Docker Compose
- **GitHub Actions** (CI/CD)
- **AWS EC2** & **ECR**
- **SonarCloud** (Code Quality)
- **Snyk** (Security Scanning)

---

## 🎯 Project Goals

- Create a minimal yet well-documented and robust Python service
- Serve the app on **port 80**
- Containerize the app using **Docker**
- Automate full deployment via **CI/CD with GitHub Actions**
- Integrate **SonarCloud** and **Snyk** for code and security checks
- (Optional) Connect the EC2 instance to a domain name via **Route 53**

---

## 🚀 CI/CD Pipeline Overview

### 🔧 Continuous Integration (CI)

On each push to the repository:

- 🧪 Run unit tests (if any)
- 🔍 Run static code analysis with **SonarCloud**
- 🛡️ Scan for vulnerabilities with **Snyk**
- 🐳 Build the Docker image
- 📤 Push the Docker image to **AWS ECR**

### 🚢 Continuous Deployment (CD)

- The EC2 instance listens for image updates
- GitHub Actions connects via SSH to:
  - Pull the latest Docker image from ECR
  - Restart the Docker container
- App is redeployed with **minimal downtime**

---

## 🧪 Local Development

### 1. Run the app locally

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python main.py
>>>>>>> develop
