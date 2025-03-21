# Hello Docker - A Simple Hello World Container

## Project Overview
This project is a beginner-friendly Docker setup where we create a simple container that prints **"Hello, Docker from VS Code with Git!"**. The purpose of this project is to:
- Learn how to create and run a Docker container.
- Understand the structure of a **Dockerfile**.
- Use **Git** for version control and push changes to **GitHub**.
- Work with **VS Code** and **Docker Desktop**.

---

## Steps Followed

### 1️⃣ Setting Up the Project
- Created a project folder `hello-docker` in VS Code.
- Initialized a Git repository:
  ```sh
  git init
  ```
- Created a `.gitignore` file to ignore unnecessary files:
  ```sh
  echo "*.log
__pycache__/
node_modules/
.env" > .gitignore
  ```
- Committed the changes:
  ```sh
  git add .gitignore
  git commit -m "Added .gitignore file"
  ```

---

### 2️⃣ Creating the Dockerfile
- Created a `Dockerfile` inside `hello-docker`.
- Added the following content:
  ```dockerfile
  # Use a minimal base image
  FROM alpine:latest
  
  # Set the default command
  CMD ["echo", "Hello, Docker from VS Code with Git!"]
  ```
- Committed the changes:
  ```sh
  git add Dockerfile
  git commit -m "Added Dockerfile for Hello World container"
  ```

---

### 3️⃣ Building the Docker Image
- Built a Docker image using:
  ```sh
  docker build -t hello-docker .
  ```
- Verified the image was created:
  ```sh
  docker images
  ```
  **Expected Output:**
  ```
  REPOSITORY      TAG       IMAGE ID       CREATED         SIZE
  hello-docker    latest    abc123xyz456   A few seconds ago  5MB
  ```

---

### 4️⃣ Running the Docker Container
- Executed the container:
  ```sh
  docker run hello-docker
  ```
- **Expected Output:**
  ```
  Hello, Docker from VS Code with Git!
  ```

---

### 5️⃣ Pushing to GitHub
- Added a remote GitHub repository:
  ```sh
  git remote add origin <your-repo-url>
  ```
- Pushed the code:
  ```sh
  git push -u origin main
  ```

---

## Final Results ✅
- Successfully created and ran a **Hello World** Docker container.
- Learned how to:
  - Write a `Dockerfile`.
  - Build and run a Docker container.
  - Use Git for version control.
  - Work with VS Code and Docker Desktop.
- Pushed the project to GitHub for future reference.

---

## Next Steps 🚀
- Modify the **Dockerfile** to run a simple web server.
- Learn about **container networking** and **volumes**.
- Experiment with **Docker Compose** for multi-container setups.

💡 **Happy Dockering!** 🐳
