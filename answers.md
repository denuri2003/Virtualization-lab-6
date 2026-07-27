# CCS3308 – Virtualization and Containers
## Lab 06 – Kubernetes Fundamentals with Minikube

### Checkpoint Question 1
**What is the difference between the Kubernetes Control Plane and a Worker Node?**

The Control Plane is responsible for managing the Kubernetes cluster. It schedules Pods, keeps track of the cluster's state, and makes sure everything is running correctly. Worker Nodes are the machines that actually run the application Pods and containers.

---

### Checkpoint Question 2
**Why does the Pod IP change after deleting and recreating a Pod?**

A Pod is temporary in Kubernetes. When it is deleted, Kubernetes creates a completely new Pod instead of restoring the old one. Because it is a new Pod, it receives a new IP address.

---

### Checkpoint Question 3
**How does Kubernetes automatically recreate deleted Pods?**

The Deployment constantly checks whether the required number of Pods is running. If one Pod is deleted, Kubernetes notices that the number of replicas has decreased and automatically creates a new Pod. This is known as the self-healing feature.

---

### Checkpoint Question 4
**Why can the frontend Deployment be scaled independently?**

Each Deployment manages only its own application. This means the frontend can be scaled without affecting the API, cache, or database, allowing resources to be managed more efficiently.

---

### Checkpoint Question 5
**What is the difference between a Pod and a Service?**

A Pod is the smallest unit in Kubernetes and contains one or more containers that run an application. A Service provides a permanent network address so users and other applications can access the Pods, even if the Pods are recreated.

---

### Checkpoint Question 6
**How are Kubernetes rolling updates different from Docker Compose updates?**

Docker Compose usually recreates containers during an update, which may briefly interrupt the application. Kubernetes performs rolling updates by replacing Pods one at a time, allowing the application to remain available while the update is taking place.

---

### Checkpoint Question 7
**Why was PostgreSQL deployed as a StatefulSet instead of a Deployment?**

PostgreSQL stores important data, so it needs stable storage and a consistent identity. StatefulSets provide persistent storage, fixed Pod names, and controlled startup and shutdown, making them more suitable for databases.

---

### Checkpoint Question 8
**How does a PersistentVolumeClaim prevent data loss?**

A PersistentVolumeClaim (PVC) stores data outside the Pod. If the Pod is deleted or restarted, Kubernetes reconnects the same storage volume, so the database information is not lost.

---

### Checkpoint Question 9
**Why did the broken Pod fail to start?**

The Pod used an invalid container image (`nginx:definitely-not-a-real-tag`). Since this image does not exist, Kubernetes could not download it. As a result, the Pod entered the `ErrImagePull` and `ImagePullBackOff` states.
