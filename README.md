# 🚀 Spring Boot CI/CD Demo

This project is a simple Spring Boot application used to demonstrate a **complete CI/CD pipeline** with **Jenkins**, **Docker**, **GitLab**, and **cloud deployment**.

---

## 🧰 Tech Stack

- Java 11  
- Maven  
- Spring Boot  
- Docker  
- Jenkins  
- GitLab  
- MySQL (remote)  
- AWS EC2 (Ubuntu)  
- NGINX  
- Cloudflare + Certbot SSL  

---

## 📁 Project Structure

```
src/
  main/java/       # App source code
  test/java/       # Unit tests
pom.xml            # Maven configuration
Dockerfile         # Docker container definition
Jenkinsfile        # CI/CD pipeline definition
```

---

## 🧪 Running the Application Locally

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/spring-boot-cicd-demo.git
cd spring-boot-cicd-demo
```

2. **Build the project:**

```bash
mvn clean install
```

3. **Run locally:**

```bash
mvn spring-boot:run
```

The app will be available at `http://localhost:8080`.

---

## 🐳 Running with Docker

1. **Build Docker image:**

```bash
docker build -t spring-boot-cicd-demo .
```

2. **Run container:**

```bash
docker run -p 8080:8080 spring-boot-cicd-demo
```

---

## 🤖 CI/CD Pipeline Overview

### ✅ GitLab → Jenkins → Docker → Cloud

1. **Code pushed to GitLab**
2. **Webhook triggers Jenkins job**
3. **Jenkins:**
   - Clones repo
   - Builds with Maven
   - Builds Docker image
   - Pushes to Docker Hub
   - SSHs into remote EC2 server
   - Pulls latest image & runs container

### ✅ Continuous Delivery Done Right

- **Automated Builds**  
- **Containerized Deployments**  
- **No manual steps** after Git push  
- **Ready for scaling and team collaboration**

---

## 🌐 Deployment Info

- Deployed on **AWS EC2** instance
- **NGINX** used as reverse proxy
- **HTTPS enabled** via **Certbot**
- **Cloudflare** used for DNS & subdomain management

---


## 📬 Feedback / Contact

Want a walk-through, explanation, or have feedback? Open an issue or reach out!


