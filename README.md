This project contains a sample Helm chart for deploying resources to Kubernetes. The Docker image used for deployment is available on Docker Hub at: https://hub.docker.com/r/foconer/springboot-helloworld

This project was tested on macOS Sequoia 15 using Docker Desktop and Minikube v1.38.0

Prerequisite (local deployment)
* Install Docker Desktop (29.1.5+) include the kubectl CLI
* Install minikube

Deployment Instruction
* Start Docker and Minikube, then verify using the following commands
  - docker container ls (check to see that minikube container is running)
  - kubectl get nodes (check that a nodes exists)
* Open a terminal
  - Clone this repository
  - Go to the project directory
* Run the following commands
  - helm install springboot .
  - kubectl get pods
  - kubectl get svc
* On macOS, running minikube tunnel is required to access the springboot-app service
  - minikube service springboot-app
  - Use the tunnel URL to access the application, generated URL example http://127.0.0.1:52883)
