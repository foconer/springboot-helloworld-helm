This project contains a sample Helm chart used to deploy resources to Kubernetes. The project image deployed is found in Docker Hub, https://hub.docker.com/r/foconer/springboot-helloworld.

This was tested in MacOS Sequoia 15, Docker Desktop, minikube v1.38.0

Prerequisite (local deployment)
* Install Docker Desktop (29.1.5+) include the kubectl CLI
* Install minikube

Deployment Instruction
* Start docker and minikube, check with commands
  - docker container ls (check to see that minikube container is running)
  - kubectl get nodes (check that a nodes exists)
* Clone this repository
* Go to Terminal and run the following commands
  - go to the project directory
  - helm install springboot .
  - kubectl get pods
  - kubectl get svc
* If using MacOS, a minikube tunnel is needed to access the springboot-app instance
  - minikube service springboot-app
  - Use the tunnel URL to access the application, generated URL example http://127.0.0.1:52883)
