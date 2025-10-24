# Jenkins–Maven Integration Project

## Overview
This project demonstrates how to integrate Jenkins and Maven for Continuous Integration (CI).  
It automates building, testing, and deploying Java applications.  
The setup includes Maven configuration, GitHub integration, and optional artifact deployment to a Nexus repository.

---

## Objectives
- Integrate Jenkins with Maven for automated builds.
- Configure Maven settings and repository access.
- Connect Jenkins to GitHub for automatic code fetching.
- Build and deploy Maven artifacts to a repository.
- Demonstrate a basic Continuous Integration workflow.

---

## Tools and Technologies
| Tool | Purpose |
|------|----------|
| Jenkins | Continuous Integration server |
| Maven 3.9.11 | Build automation tool |
| Java JDK 11/17 | Programming language and runtime |
| Git & GitHub | Version control system |
| Nexus Repository | Artifact repository (optional) |
| Windows/Linux | Operating environment |

---

## Setup and Configuration

### Step 1: Install Required Tools
1. Install **Java JDK** and add it to the system PATH.
2. Install **Apache Maven (3.9.x)** and configure environment variables.
3. Install **Jenkins** and start it at `http://localhost:8080`.
4. Install **Git**.

---

### Step 2: Configure Jenkins
1. Open **Manage Jenkins → Global Tool Configuration**.
2. Add the following:
   - JDK (if not auto-detected)
   - Maven (example: `maven 3.9.11`)
   - Git Plugin

---

### Step 3: Create and Push a Maven Project to GitHub
```bash
mvn archetype:generate
git init
git add .
git commit -m "Initial Maven project"
git remote add origin https://github.com/<username>/jenkins-maven-project.git
git push -u origin main
