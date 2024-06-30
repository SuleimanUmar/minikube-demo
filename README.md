**Kubernetes Crash Course Summary:**

- **Core Concepts:** Learned foundational concepts such as Pods, Deployments, Services, and Labels in Kubernetes.
  
- **Main Kubernetes Components:** Explored key components like `kubectl`, Pods, Deployments, Services, and ConfigMaps.

- **Kubernetes Configuration File:** Understood the structure and syntax of Kubernetes YAML configuration files used for creating and managing Kubernetes resources.

- **Local Kubernetes Cluster Setup:** Learned how to set up and manage a local Kubernetes cluster using tools like Minikube or Docker Desktop Kubernetes.

- **Hands-On Demo Project:** Implemented a basic web application with a database deployment on a local Kubernetes cluster. Covered steps from defining YAML configurations to deploying and accessing the application.

- **Practical Application Setup:** Gained practical experience in deploying and configuring applications on Kubernetes, laying a foundation for more complex deployments in production environments.

#### K8s manifest files 
* mongo-config.yaml
* mongo-secret.yaml
* mongo.yaml
* webapp.yaml

#### K8s commands

##### start Minikube and check status
    minikube start --vm-driver=hyperkit 
    minikube status

##### get minikube node's ip address
    minikube ip

##### get basic info about k8s components
    kubectl get node
    kubectl get pod
    kubectl get svc
    kubectl get all

##### get extended info about components
    kubectl get pod -o wide
    kubectl get node -o wide

##### get detailed info about a specific component
    kubectl describe svc {svc-name}
    kubectl describe pod {pod-name}

##### get application logs
    kubectl logs {pod-name}
    
##### stop your Minikube cluster
    minikube stop

<br />

> :warning: **Known issue - Minikube IP not accessible** 

If you can't access the NodePort service webapp with `MinikubeIP:NodePort`, execute the following command:
    
    minikube service webapp-service

<br />

#### Links
* mongodb image on Docker Hub: https://hub.docker.com/_/mongo
* webapp image used Docker Hub: https://hub.docker.com/repository/docker/nanajanashia/k8s-demo-app
* k8s official documentation: https://kubernetes.io/docs/home/
