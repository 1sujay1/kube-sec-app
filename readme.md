Start with these commands:

npm init -y
npm i express

create Dockerfile,app.js,.ignore,.dockerignore

create a simple server using express
Build a simple node-alpine image

Execute Docker Compose File:
docker-compose up -d --build

To Stop Container yaml file
docker-compose down

---

kubectl commands:

kubectl create deployment first-app --image=sujaygowdag333/kube-first-app
kubectl get deployments
kubectl get pods
kubectl get services
kubectl delete deployment first-app
kubectl expose deployment first-app --type=LoadBalancer --port=8080

minikube service first-app : To get ip address of remote machine
minikube tunnel

To Scale :
kubectl scale deployment/first-app --replicas=3

To Update Image
kubectl set image deployment/first-app kube-first-app=sujaygowdag333/kube-first-app

To get deployed status
kubectl rollout status deployment/first-app

To Undo the updated image
kubectl rollout undo deployment/first-app

To Get deployment history
kubectl rollout history deployment/first-app

To Get deployment details
kubectl rollout history deployment/first-app --revision 2

To Go to Particular deployed revision
kubectl rollout undo deployment/first-app --to-revision=5

To Get Storage Classes
kubectl get sc

To Get Persistent Volumes
kubectl get pv

To Get Persistent Volume Claim
kubectl get pvc

To Get ConfigMap (environmental variables)
kubectl get configmap

---

To Run using Yaml file
kubectl apply -f=deployment.yaml
OR
kubectl apply -f .\deployment.yaml
kubectl apply -f .\service.yaml

To Delete using Yaml file

kubectl delete -f .\deployment.yaml -f .\service.yaml

To delete Labels
kubectl delete deployments,services -l group=example
