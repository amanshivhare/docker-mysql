
# docker-mysql

This project demonstrates how to run a Spring Boot application with a MySQL database using Docker.

## Getting Started

Follow the steps below to build and run the project using Docker and Docker Compose:

---

### 1. **Extract and Build the Project**
- Unzip the project archive.
- Navigate to the root directory and run:
  ```bash
  mvn clean install
  ```

---

### 2. **Login to Docker Hub**
- Open a terminal and run:
  ```bash
  docker login
  ```
- Enter your Docker Hub username and password when prompted.

> If login fails, your Docker installation may be outdated. Try the following commands:
```bash
sudo apt update
sudo apt upgrade docker-ce
```

---

### 3. **Build the Docker Image**
- Navigate to the project directory containing the `Dockerfile` (e.g., `docker-mysql`) and run:
  ```bash
  docker build -t your-dockerhub-username/image-name:tag .
  ```
- Replace:
  - `your-dockerhub-username` with your Docker Hub username
  - `image-name` with your desired image name
  - `tag` with a version label (e.g., `0.0.1`)

---

### 4. **Run Docker Compose**
- From the same directory where `docker-compose.yml` is located, run:
  ```bash
  docker-compose up
  ```

---

### 5. **Verify Running Containers**
- After successful startup, check running containers using:
  ```bash
  docker ps
  ```
- You should see two containers:
  - Spring Boot application running on a specific IP and port
  - MySQL database container on another port

---

### 6. **Test the Application**
- Use the IP and port from the Boot application container to test the APIs via Postman or any REST client.

---

### 7. **Access the MySQL Container**
- To connect to the MySQL container, run:
  ```bash
  docker exec -it <container_id> bash
  ```
- Replace `<container_id>` with the actual container ID of the MySQL container.
