# 🐳 Docker Essentials & Quick Guide

## 📌 Core Concepts

| Concept | Description |
| :--- | :--- |
| **Image Sharing** | People share **Docker Images** (not running containers) via registries like Docker Hub. An image is a read-only template or blueprint. |
| **Resource Usage** | **Docker Containers** consume active system memory (RAM) and CPU resources when running, whereas images primarily consume disk storage. |

---

## 💻 Essential Docker Commands

### 1. Download Docker Image (`Download image`)
To download a Docker image from a registry to your local system, use the `pull` command:

```cmd
docker pull image_name
```
### 2. Run Container from the Image (`run container from image`)
To create and start a container using a downloaded Docker image, execute the following command in your terminal:

```cmd
docker run image_name
```
### 3. Run Container in Interactive Mode (`-it`)
To run a container interactively (so you can access its terminal shell and type commands directly inside it), use the following command:

```cmd
docker run -it image_name
```
### 4. List All Containers (`docker ps -a`)
To view a list of **all containers** on your system—including both currently running containers and those that have stopped—execute the following command:

```cmd
docker ps -a
```
### 5. List Running Containers (`docker ps`)
To view a list of **currently running containers** on your system, execute the following command:

```cmd
docker ps
```
### 6. Start an Existing Container (`docker start`)
To start a container that has already been created or previously stopped, use the following command:

```cmd
docker start container_id_or_name
```
### 7. To stop Container that already running now (`Docker Stop`)
```cmd
docker stop container_id_or_name
```
### 8. List Local Docker Images (`docker images`)
To view a list of all **Docker images** currently downloaded and saved on your local system, execute the following command:

```cmd
docker images
```
### 9. Delete a Stopped Container (`docker rm`)
To permanently delete or remove one or more **stopped containers** from your local system to free up storage, execute the following command:
```cmd
docker rm container_id_or_name
```
### ⚠️ Important Note: Order of Deletion (`Container vs. Image`)

When cleaning up your local Docker environment, you **must delete the container first** before you can delete its corresponding image. 

#### Why?
* Docker prevents you from deleting an image if there are any stopped or running containers dependent on it.
* If you try to delete an image directly while a container uses it, Docker will throw an error.

#### Correct Cleanup Sequence:
1. **Stop the container:**
```cmd
docker stop container_id_or_name
```

### 10. Delete Local Docker Image (`docker rmi`)
To delete or remove one or more **Docker images** from your local system and free up disk space, execute the following command:

```cmd
docker rmi image_name_or_id
```