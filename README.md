# Guestbook Application Deployment with Docker & Kubernetes on IBM Cloud

## 🚀 Overview
This project was built as a final assignment for the Coursera course:  
**"IBM Containers & Kubernetes Essentials with Docker and OpenShift"**.

The application is a simple Guestbook web app, containerized with Docker, deployed using Kubernetes, and hosted on IBM Cloud. The project demonstrates:
- Docker image creation and deployment
- Kubernetes deployments, services, and autoscaling
- Rolling updates and rollback strategies

---

## 🛠️ Technologies Used
- Docker
- Kubernetes (kubectl)
- IBM Cloud Kubernetes Service
- Horizontal Pod Autoscaler (HPA)
- Docker Registry (IBM Cloud Container Registry)

---

## 📂 Project Structure

- `Dockerfile`: Defines the container for the guestbook app
- `guestbook-app/`: The source code of the web app
- `manifests/`: Kubernetes YAML configurations
- `screenshots/`: Visual proof for each deployment and configuration step

---

## ✅ Tasks Completed

| Task | Description | Screenshot |
|------|-------------|------------|
| 1 | Updated Dockerfile | ![Dockerfile](https://github.com/user-attachments/assets/c29fac02-6192-4d3c-8957-811fa723acf6) |
| 2 | Pushed image to IBM Container Registry | ![crimages](https://github.com/user-attachments/assets/7d4d01d0-fa67-4150-a0cb-99d51acc153d) |
| 3 | Deployed index page (v1) | ![app](https://github.com/user-attachments/assets/f7430f68-3813-491c-aaa6-bdcd8b6c62c5) |
| 4 | Created Horizontal Pod Autoscaler | ![hpa](https://github.com/user-attachments/assets/9a82a086-e262-4445-a5c1-6ad1e045f63d) |
| 5 | Verified Autoscaler scaling pods | ![hpa2](https://github.com/user-attachments/assets/b6a027ac-5248-4200-a167-ce9c35568807) |
| 6 | Docker build & push for v2 | ![upguestbook](https://github.com/user-attachments/assets/5a5bdd74-9e5b-41ec-9a18-409da92207c7) |
| 7 | Deployment configured for autoscaling | ![deployment](https://github.com/user-attachments/assets/997e9dbb-79c4-4312-a37b-f84d1b4aeb12) |
| 8 | Updated index page (v2) after rollout | ![up-app](https://github.com/user-attachments/assets/353a4ed2-b988-47fc-bf2e-7cc39dec2b94) |
| 9 | Deployment revision history | ![rev](https://github.com/user-attachments/assets/3287187b-dcbe-46e4-b73e-297a6ba5db17) |
| 10 | Rollback verification | ![rs](https://github.com/user-attachments/assets/bd8afda9-782e-4031-b80b-98fca7f1f9bd) |

---


## 📦 How to Run 
If you want to replicate this:

1. Clone the repo:
```bash
git clone https://github.com/yourusername/guestbook-k8s-deployment.git
cd guestbook-k8s-deployment
```

2. Build and push Docker image:

```bash
docker build -t us.icr.io/YOUR_NAMESPACE/guestbook:v1 .
docker push us.icr.io/YOUR_NAMESPACE/guestbook:v1
Apply Kubernetes manifests:
```

3. Apply Kubernetes manifests:

```bash
kubectl apply -f manifests/deployment-v1.yaml
kubectl apply -f manifests/service.yaml
Enable autoscaling:
```

4. Enable autoscaling:

```bash
kubectl apply -f manifests/hpa.yaml
Rollout v2:
```

5. Rollout v2:

```bash
kubectl apply -f manifests/deployment-v2.yaml
Rollback if needed:
```

6. Rollback if needed:

```bash
kubectl rollout undo deployment/guestbook
```

## 👨‍🎓 Author
Hossam Jame

Final Project for IBM Containers and Kubernetes Essentials with Docker and OpenShift
Completed on: July 2025


