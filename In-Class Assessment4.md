1. What problem does serverless computing aim to solve compared to traditional microservice deployment on Kubernetes? Give one example where serverless is clearly better, and one where it may not be.


Serverless computing aims to abstract away infrastructure management and reduce operational overhead compared to traditional microservice deployments on Kubernetes. It allows developers to focus solely on application logic without worrying about provisioning, scaling, or maintaining servers. Serverless is clearly better for applications with highly variable workloads, such as event-driven image processing where requests can spike unpredictably. Conversely, it may not be suitable for applications requiring long-running processes or strict latency guarantees, such as real-time video streaming, because cold starts and execution limits can impact performance.


2. What are the advantages of using a service mesh (like Istio) for managing microservices communication instead of relying only on Kubernetes networking?


A service mesh like Istio provides fine-grained control over service-to-service communication, including traffic routing, observability, and security, which Kubernetes networking alone cannot fully manage. It allows features such as mutual TLS encryption, distributed tracing, and intelligent retries without modifying application code. This improves reliability, security, and operational insight, particularly in large-scale microservice architectures with complex interactions.


3. Explain what a sidecar proxy (such as Envoy in Istio) does. Why is it needed in a service mesh?


A sidecar proxy is deployed alongside each microservice instance to intercept all incoming and outgoing traffic. In a service mesh, the sidecar handles responsibilities like routing, load balancing, encryption, and telemetry on behalf of the application. It is needed because it decouples these cross-cutting concerns from the application code, allowing consistent traffic management and security policies across all services without requiring developers to implement them manually.


4. What kind of traffic management features does Istio provide? Give two examples of how they can be useful in production systems.


Istio provides traffic management features such as weighted routing, retries, circuit breaking, and fault injection. Weighted routing can be useful to gradually roll out a new version of a service to a subset of users for canary testing, minimizing risk. Retries and circuit breaking improve resilience by automatically retrying failed requests or preventing cascading failures when a service is under high load, maintaining overall system stability.


5. Explain how Knative Serving enables autoscaling for an application. What triggers scaling up and scaling down?


Knative Serving enables autoscaling by monitoring incoming request traffic and automatically adjusting the number of running pods. Scaling up is triggered when the request rate exceeds the current processing capacity, while scaling down occurs when traffic decreases, potentially down to zero for idle services. This dynamic scaling ensures efficient resource utilization while maintaining responsiveness for variable workloads.


6. What is the role of Knative Eventing, and how does it support event-driven architectures?


Knative Eventing provides a framework for routing and delivering events between producers and consumers, enabling loosely coupled, event-driven architectures. It supports various event sources, such as HTTP requests, messaging systems, or cloud services, and delivers events reliably to services or functions. By decoupling event producers and consumers, it allows developers to build reactive applications that respond dynamically to real-time events.


7. How does Knative leverage Kubernetes primitives to provide a serverless experience? Discuss which components of Kubernetes (e.g., Deployments, Services, Horizontal Pod Autoscaler) are abstracted away and how this abstraction benefits developers.


Knative leverages Kubernetes primitives like Deployments, Services, and Horizontal Pod Autoscalers to manage workloads, networking, and scaling while exposing a simplified serverless interface to developers. For example, Knative abstracts pod creation, scaling rules, and service routing, allowing developers to deploy applications without directly configuring these Kubernetes objects. This abstraction reduces operational complexity and accelerates development by letting developers focus on application logic instead of infrastructure details.


8. In KServe, what is the main function of an InferenceService, and how does it simplify deploying ML models?


In KServe, an InferenceService is a high-level Kubernetes custom resource that defines the complete serving configuration for a machine learning model, including the predictor, transformer, and explainer components. It simplifies deployment by automating tasks such as container creation, scaling, routing, and monitoring, allowing data scientists to deploy models without writing extensive Kubernetes manifests or managing individual microservices.


9. In a production ML workflow using KServe, describe how data moves from an incoming HTTP request to a model prediction response. Which layers (Knative, Istio, KServe, Kubernetes) handle which responsibilities, and where could latency bottlenecks occur?


In a KServe production workflow, an HTTP request first enters the Istio ingress gateway, which handles routing and security. The request is then forwarded to a Knative service that manages pod scaling and load balancing. KServe routes the request to the appropriate predictor container running on Kubernetes, executes the model inference, and returns the response through the same layers. Latency bottlenecks may occur at the Istio proxy layer due to encryption and routing overhead, during model loading if cold starts happen, or in the Knative autoscaler when scaling from zero pods.


10. How can Istio’s traffic routing capabilities (e.g., weighted routing, retries, circuit breaking) be used to support canary deployments or A/B testing in Knative or KServe environments? Discuss the pros and cons compared to manual rollout strategies.


Istio’s traffic routing capabilities allow directing a controlled percentage of traffic to new service versions, enabling canary deployments or A/B testing without downtime. Weighted routing can gradually shift traffic, retries ensure reliability, and circuit breaking protects against failures. Compared to manual rollouts, this approach reduces risk, allows faster feedback, and provides real-time monitoring of the new version’s performance. However, it adds complexity to configuration and may require expertise in service mesh policies, which can be more challenging to debug than simple manual deployments.
