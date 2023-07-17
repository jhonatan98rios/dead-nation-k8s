

## Commands

### Build:
    - docker build -t jhonatan98rios/express-google-oauth2 .

### Run:
    - docker run -d -p 5000:5000 --name express-google-oauth2 --rm jhonatan98rios/express-google-oauth2

### Push:
    - docker push jhonatan98rios/express-google-oauth2

### Config
    - kubectl config view

### Create Deployment Imperatively
    - kubectl create deployment express-google-oauth2-deployment --image=jhonatan98rios/express-google-oauth2

### List Deployments
    - kubectl get deployments

### Describe Deployments
    - kubectl describe deployments

### List Pods
    - kubectl get pods

### Describe Pods
    - kubectl describe pods

### Create a Service Imperatively
    - kubectl expose deployment express-google-oauth2-deployment --type=LoadBalancer --port=5000

### Generate IP Service from Minikube
    - minikube service express-google-oauth2-deployment # Imperatively
    - minikube service express-google-oauth2-service # Declaratively

### List Services
    - kubectl get services

### Describe Service
    - kubectl describe services/express-google-oauth2-deployment

### Update Application Image
    - kubectl set image <deployment> <container>=<docker-image>:<tag>
    - kubectl set image deployment/express-google-oauth2-deployment express-google-oauth2=jhonatan98rios/express-google-oauth2:0.0.2

### Rollback Status
    - kubectl rollout status deployment/express-google-oauth2-deployment

### Rollback Undo
    - kubectl rollout undo deployment/express-google-oauth2-deployment

### Execute yml file
    - kubectl apply -f <file>
    - kubectl apply -f deployment.yaml

## Delete file
    - kubectl delete -f <file>
    - kubectl delete -f deployment.yaml