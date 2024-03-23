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
* Containers vs VMs
  - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture1.png?raw=true =250x500)
* Container vs Image <image>
  - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture2.png?raw=true)
  - An image is a package or a template, just like a VM template that you might have worked with in the visualization world. It is used to create one ormore containers.
  - Containers are running instances off images that are isolated and have their own environments and set of processes.
  b. Orchestration
2. Kubernetes Concepts - PODs | ReplicaSets | Deployment | Services
  a. PODs
    - A POD is a single instance of an application. A POD is the smallest object, that you can create in Kubernetes
    - Kubernetes deploys containers into PODs <image>
    - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture3.png?raw=true)
    ? If the number of users accessing the application increases and we need to scale the application, would we spin up additional instances? Do we bring up a new container within the same POD? => Answer: We create a new POD altogether with a new instance of the same application
    => If the user base further increases, we can always deploy new additional PODs on a new node in the cluster. We now have a new node added to the cluster to expand the cluster's physical capacity
      - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture4.png?raw=true)
    => PODs usually have a 1-on-1 relationship with containers running your application. To scale UP you create new PODs, to scale DOWN you delete PODs.
    - Multicontainer PODs
      + A POD can have multiple containers, but not of the same type (Like a web app with a helper) <image>
      - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture5.png?raw=true)
      + The two containers can also communicate with each other directly by referring to each other as 'localhost' since they share the same network namespace.
    - If we want to link a new helper container with our app, we can establish a network connectivity between the app and the helper, and Kubernetes does this automatically <image>
    - ![alt text](https://github.com/PluckySquirrel/Kubernetes_GR_Repo/blob/master/Images/Picture6.png?raw=true)
3. Introduction to YAML
4. Networking in Kubernetes
5. Kubernetes Management - Kubectl
6. Kubernetes Definition Files - YAML
7. Kubernetes on Cloud - AWS/GCP
