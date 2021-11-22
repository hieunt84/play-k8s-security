### 01. Chuẩn bị cluster k8s với minikube
```
minikube start
```

### 02. Add repo happyit
```
helm repo add happyit  https://raw.githubusercontent.com/hieunt84/play-k8s-helm/master/
```

### 03. Deploy app myngix
```
helm install nginx happyit/mynginx
```

### 04. kiểm tra default service account
```
kubectl get service account
```