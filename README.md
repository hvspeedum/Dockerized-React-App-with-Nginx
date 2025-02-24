# 🚀 Containerized Deployment of React App with Nginx  

This repository demonstrates the **containerized deployment** of a **React application** using **Docker** and **Nginx**. The project follows a **multi-stage build approach** to optimize the image size and improve performance.  

---

## 📌 Features  

### ✅ **Containerized React Application**  
- Uses **Docker** to create an isolated, portable environment for the React app.  
- Optimized **multi-stage build** to reduce the final image size.  

### ✅ **Deployment with Nginx**  
- Serves the **React app** using an **Nginx web server** for better performance.  
- Exposes the application on **port 80** to be accessed in a browser.  

## ⚙️ **How to Run the Application**  

### 🔹 **1. Prerequisites**  
Ensure you have the following installed:  
- [Node.js](https://nodejs.org/)  
- [Docker](https://www.docker.com/)  

### 🔹 **2. Build and Run the Docker Container**  

### 🛠️ Build the Docker Image  
```sh
docker build -t react-nginx-app .
```

### 🚀 Run the Container
```sh
docker run -d -p 80:80 react-nginx-app
```

The React app will be accessible at: http://localhost

### ✅ **Future Enhancements**  
- **Jenkins CI/CD integration** for automated build and deployment.  
- **Cloud deployment (AWS, Azure, GCP)** for scalability and availability.  
- **Nginx configuration optimizations** for better caching and security.  
