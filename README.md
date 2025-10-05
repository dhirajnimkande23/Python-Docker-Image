# Python-Docker-Image
Dockerize python code into container


📦 Python Hello World Docker Project
This guide will walk you through creating a simple Python Hello World app, containerizing it with Docker, and running it locally.

git clone https://github.com/atulkamble/pythonhelloworld.git
cd pythonhelloworld
📁 Project Structure
.
├── Dockerfile
└── helloworld.py
📜 Steps to Build and Run
1️⃣ Create Python Hello World Script
touch helloworld.py
Open and add the following code:

print("Hello, World from Dockerized Python App!")
Check the file:

cat helloworld.py
Run it locally to test:

python3 --version
python3 helloworld.py
2️⃣ Create Dockerfile
touch Dockerfile
Edit and add the following content:

# Use official Python base image
FROM python:3.12-slim

# Set working directory
WORKDIR /app

# Copy local code to the container
COPY helloworld.py .

# Command to run the app
CMD ["python", "helloworld.py"]
Check files:

ls
3️⃣ Build Docker Image
docker build -t dhiraj23/pythonhelloworld .
Check Docker images:

docker images
4️⃣ Push Docker Image to Docker Hub
docker push dhiraj23/pythonhelloworld
5️⃣ Pull Image (if testing from another system)
docker pull dhiraj23/pythonhelloworld
6️⃣ Run Docker Container
docker run atuljkamble/pythonhelloworld
Check running containers:

docker container ls
docker ps -a
✅ Output Example
Hello, World from Dockerized Python App!
📌 Notes
Make sure you are logged in to Docker Hub before pushing:

docker login
