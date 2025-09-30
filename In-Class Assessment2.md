1. Orchestration tools, such as Kubernetes, play a key role in the server infrastructure for the modern applications.

(a) Explain how these tools help manage and scale application servers.

Automatically manage servers and automatically scale them up and down based on load to ensure high availability.

(b) Describe how orchestration tools facilitate automated deployment, scaling, and management of application servers.

Provides functions such as automatic deployment (rolling update), automatic scaling, and fault self-healing.

2. Explain the difference between a Pod, Deployment, and Service.

Pod: The smallest deployment unit, a collection of containers

Deployment: Manages Pod replication and updates

Service: Provides access and load balancing for Pods

3. What is a Namespace in Kubernetes? Please list one example.

Resource isolation mechanism

Example: kube-system

4. Explain the role of the Kubelet. How do you check the nodes in a Kubernetes cluster? (kubectl command expected)

Ensure that the Pod runs on the node and communicates with the API Server

command: kubectl get nodes

5. What is the difference between ClusterIP, NodePort, and LoadBalancer services?

ClusterIP: Access within the cluster

NodePort: Access via a node port

LoadBalancer: Cloud Load Balancer for external access

6. How do you scale a Deployment to 5 replicas using kubectl?

kubectl scale deployment <name> --replicas=5

7. How would you update the image of a Deployment without downtime?

kubectl set image deployment/<name> <container>=<new-image>

8. How do you expose a Deployment to external traffic?

kubectl expose deployment <name> --type=NodePort --port=80

9. How does Kubernetes scheduling decide which node a Pod runs on?

The scheduler selects nodes based on resources, constraints, and load balancing

10. What is the role of Ingress and how does it differ from a Service?

Service: Provides network access for Pods

Ingress: Provides HTTP routing based on domain names and paths
