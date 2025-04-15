# docker

📄 README.md
markdown
Copy
Edit
# 🐳 Dockerized Flask App

A simple Python Flask web app running inside a Docker container. This project demonstrates how to build, run, and manage containers using Docker and Docker Desktop.

---

## 📁 Project Structure

my-python-app/ │ ├── app.py # Main Flask application ├── requirements.txt # Python dependencies ├── Dockerfile # Docker build instructions └── README.md # Project documentation

yaml
Copy
Edit

---

## 🚀 Getting Started

### 1. Prerequisites

- ✅ [Docker Desktop](https://www.docker.com/products/docker-desktop) installed and running  
- ✅ [Visual Studio Code](https://code.visualstudio.com/) (optional, but recommended)
- ✅ Python not required on host (everything runs in container)

---

### 2. Clone the Repository

```bash
git clone https://github.com/your-username/my-python-app.git
cd my-python-app
3. Build the Docker Image
bash
Copy
Edit
docker build -t my-python-app .
4. Run the Docker Container
bash
Copy
Edit
docker run -d -p 5000:5000 --name flask-container my-python-app

![Screenshot 2025-04-14 193651](https://github.com/user-attachments/assets/788d86e3-f021-4c47-bdfe-83efc2985a5d)


5. Check the App in Docker Desktop
Open Docker Desktop and go to the Containers & Apps tab:



✅ See flask-container running

📜 Click to view logs

💻 Use the built-in CLI to access the container shell

🔁 Start / Stop / Restart / Delete the container as needed

6. View the Web App in Browser (Optional)
Open your browser and visit:

arduino
Copy
Edit
http://localhost:5000
You should see: Hello from Docker!

![Screenshot 2025-04-14 193558](https://github.com/user-attachments/assets/4def6299-36e8-4a07-a91f-b5a570352b70)

🧰 Useful Docker Commands
bash
Copy
Edit
# List running containers
docker ps




# List all containers (including stopped)
docker ps -a



![Screenshot 2025-04-14 193638](https://github.com/user-attachments/assets/e74c8031-77e8-43f9-ae2a-58110d71bed8)

# View logs
docker logs flask-container

# Open a shell inside the container
docker exec -it flask-container bash

# Stop the container
docker stop flask-container

# Remove the container
docker rm flask-container
📦 Docker Desktop Overview
Feature	Location
View running containers	Containers & Apps tab
Access logs and CLI	Click container → Logs / CLI
Manage images	Images tab
Manage volumes	Volumes tab
Start/Stop/Delete	Buttons in container row



![Screenshot 2025-04-14 193534](https://github.com/user-attachments/assets/a8c06c57-a286-4c2c-a632-f3291a1172c3)


🧼 Clean Up
bash
Copy
Edit
# Stop and remove container
docker stop flask-container
docker rm flask-container

# Remove image
docker rmi my-python-app

