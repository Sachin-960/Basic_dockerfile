### 📦 Dockerfile Project: Hello Captain!

This is a simple Docker project that uses the lightweight Alpine Linux image and prints a message using Docker's `CMD` instruction.

---

## 🛠️ Dockerfile Content

```Dockerfile
# Use the latest minimal Alpine Linux image
FROM alpine:latest

# Set the default command to run when the container starts
CMD ["echo", "Hello Captain!"]
```

---

## 📋 Why We Use These Instructions

### 🐳 `FROM alpine:latest`

- **Purpose**: It defines the base image for the Docker container.
- **Why Alpine?**:  
  - It's a **minimal Linux distribution**.
  - Only ~5 MB in size — fast to download and start.
  - Ideal for simple tasks or small utilities.

### 📢 `CMD ["echo", "Hello Captain!"]`

- **Purpose**: This sets the **default command** that runs **when a container is started** from the image.
- **Why `CMD`?**
  - `CMD` provides **runtime behavior** of the container.
  - Unlike `RUN`, which executes during build time, `CMD` executes during **container runtime**.
  - It can be **overridden** by passing a new command during `docker run`.

---

## 🚀 How to Build and Run

### 🧱 Step 1: Build the Docker image

```bash
docker build -t hello-captain .
```

### ▶️ Step 2: Run the Docker container

```bash
docker run hello-captain
```

### 🖨️ Output:

```bash
Hello Captain!
```

---

## 📚 Summary

This project is a minimal example of how Docker works with:

- **Lightweight base images (Alpine)**
- **Runtime instructions (`CMD`)**
- **Container execution that mimics a simple script**

Great for learning the basics of Dockerfile creation and container behavior.
This project is a part of [Roadmap.sh](https://roadmap.sh/projects/basic-dockerfile) Devops Projects
