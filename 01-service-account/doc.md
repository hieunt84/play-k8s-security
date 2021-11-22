### What?
```
- service account (sa) là một loại tài khoản giống với user account.
- dùng cho các services (process) chạy bên trong pod.
```

### Why?
```
- dùng để xác thực danh tính cho phép truy cập các tài nguyên trong k8s cluster.
```

### How?
```
- khi một pod được tạo ra, nếu không chỉ định sa, thì hệ thống sẽ cấp default sa.
```

### Example
```
apiVersion: v1
kind: ServiceAccount
metadata:
  name: build-robot
automountServiceAccountToken: false
...

apiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  serviceAccountName: build-robot
  automountServiceAccountToken: false
  ...
```

### Ref
```
https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/
https://medium.com/the-programmer/working-with-service-account-in-kubernetes-df129cb4d1cc

```