This lab exercise will give you hands-on experience with Knative for building, deploying, and managing serverless, cloud-native applications on Kubernetes.

Please follow the instructions here:
[Knavtive Serving and Eventing setup]

https://knative.dev/docs/install/yaml-install/serving/install-serving-with-yaml/

https://knative.dev/docs/install/yaml-install/eventing/install-eventing-with-yaml/

#Commands for your reference

minikube start   --driver=docker   --memory=15360   --cpus=8   --base-image=registry.k8s.io/kicbase/stable:v0.0.48 --kubernetes-version=v1.34.0

kubectl apply -f serving-crds.yaml
kubectl apply -f serving-core.yaml
kubectl get pods -n knative-serving

kubectl apply -f istio.yaml
kubectl get pods -A
kubectl apply -f net-istio.yaml
kubectl get pods -n istio-system
kubectl --namespace istio-system get service istio-ingressgateway

kubectl apply -f cert-manager.yaml
kubectl get pods --namespace cert-manager

kubectl apply -f eventing.yaml

[Knative Functions]
https://knative.dev/docs/getting-started/about-knative-functions/

Comments: 1. Use local registry;  2. Skip the "Deploying a function" part

#Commands for your reference
kn func version
func create -l go hello
kn func run
docker run -d -p 5001:5000 --name registry registry:2
func run --registry localhost:5001
func invoke
func build --registry locahost:5001


[Knative Serving]
https://knative.dev/docs/getting-started/first-service/

[Knative Eventing]
https://knative.dev/docs/getting-started/getting-started-eventing/


Please write a document with screenshots and notes for major steps and commit it to your github repo.


| lab9 | [Completed](lab9.docx) |
