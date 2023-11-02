## Set up
```
minikube start
kubectl get all
kubectl get nodes
```

## Test self healing arch - delete a single pod
```
kubectl apply -f nginx-deployment-withrolling.yaml
kubectl delete pod nginx-app-77544c8665-8tvr4
kubectl get all
```

## Test self healing arch - delete replica set
```
kubectl delete rs nginx-app-77544c8665
kubectl get rs
```

## Look at setup
```
kubectl describe pods
kubectl describe rs
kubectl describe deployment
```

## Update deployment
```
kubectl apply -f nginx-deployment-update.yaml
kubectl get rs --watch
kubectl get pods
```

## Remove old deployment
```
kubectl delete rs nginx-app-77544c8665
```

## Source vid for lab
```
https://www.youtube.com/watch?v=y_vy9NVeCzo&list=PLRfcTs7jiwddt8T8-fzxDD2KwapIjDj20&index=69
```