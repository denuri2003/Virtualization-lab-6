# CCS3308 – Virtualization and Containers

# Lab 06 – Kubernetes Fundamentals with Minikube

## Student Information

**Name:** Denuri Vilara

**Student ID:** YOUR STUDENT ID

**Module:** CCS3308 – Virtualization and Containers

---

# Introduction

This lab introduced the basic concepts of Kubernetes using Minikube. During the practical session, I learned how to create Pods, Deployments, Services, and StatefulSets. I also practiced scaling applications, performing rolling updates, troubleshooting failed Pods, and working with persistent storage.

---

# Software Used

- Windows 11
- Visual Studio Code
- Docker Desktop
- Minikube
- kubectl
- Kubernetes
- Git

---

# Folder Structure

```
lab6/
│
├── k8s/
├── screenshots/
├── answers.md
└── README.md
```

---

# Tasks Completed

### Part 1 – Cluster Setup
Verified that Minikube and Kubernetes were running correctly.

### Part 2 – Pod Creation
Created and deployed a standalone Nginx Pod.

### Part 3 – Deployment
Created a Deployment and observed Kubernetes automatically recreate deleted Pods.

### Part 4 – Scaling
Scaled the Deployment up and down using different replica counts.

### Part 5 – Service
Exposed the frontend application through a Kubernetes Service and accessed it in a web browser.

### Part 6 – Rolling Updates
Updated the application image and performed a rollback to the previous version.

### Part 7 – Multi-Tier Application
Deployed a simple application consisting of:
- Frontend
- API
- Cache
- PostgreSQL Database

### Part 8 – Storage and Monitoring
Verified persistent storage and monitored CPU and memory usage using the Metrics Server.

### Part 9 – Troubleshooting
Created a faulty Pod and used Kubernetes commands to identify the reason for the failure.

### Part 10 – Cleanup
Deleted all Kubernetes resources created during the lab.

---

# Technologies Used

- Kubernetes
- Minikube
- Docker
- YAML
- kubectl
- Visual Studio Code

---

# Conclusion

This lab helped me understand the core features of Kubernetes through practical activities. I learned how Kubernetes manages applications, automatically recovers failed Pods, scales workloads, exposes services, and provides persistent storage. Overall, the lab gave me valuable hands-on experience with Kubernetes fundamentals.
