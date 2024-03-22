# Kubernetes_GR_Repo
Gradual Research course for Infrastructure as Code (IaC) by Luong Nguyen Hoang Anh - 20210048 - HUST 

1. Introduction to Kubernetes
- Kubernetes also known as K8s was built by Google based on their experience running containers in production. It is now an open-source project and is arguably one of the best and most popular container orchestration technologies out there.
- To understand Kubernetes, we must understand two things - Container and Orchestration.
  a. Container
  - Containers are completely isolated environments, as in they can have their own processes or services, their own network interfaces, their own mounts, just like Virtual machines, except that they all share the same OS Kernel.
  - Some types of containers: LXC, LXD, LXCFS etc.
  - Docker utilizes LXC containers.
  - Setting up these container environment is hard as they are very low level and that is where Docker offers a high level tool with several powerful functionalities making it really easy for end users like us.
  * Containers vs VMs <image>
  * Container vs Image <image>
  - An image is a package or a template, just like a VM template that you might have worked with in the visualization world. It is used to create one ormore containers.
  - Containers are running instances off images that are isolated and have their own environments and set of processes.
  b. Orchestration
2. Kubernetes Overview
3. Kubernetes Concepts - PODs | ReplicaSets | Deployment | Services
4. Networking in Kubernetes
5. Kubernetes Management - Kubectl
6. Kubernetes Definition Files - YAML
7. Kubernetes on Cloud - AWS/GCP
