### Mục tiêu
```
Configure Access to Multiple Clusters

```

### Chuẩn bị
```
Chuẩn bị 02 Cluster k8s 1 node with kubeadm
Chuẩn bị 01 Client để kết nối với hai cluster
```

### On cluster1
```
- Tạo user demo với certificate.
- cấp quyền theo yêu cầu
- cuối cùng có file demo.kubeconfig
```

### On cluster2
```
- Tạo user hieunt với certificate.
- cấp quyền theo yêu cầu.
- cuối cùng có file demo2.kubeconfig
```

### On client
```
- cài đặt kubectl
- download demo.kubeconfig từ cluster1
- download demo2.kubeconfig từ cluster2
- tạo thư mục ~/.kube
- copy file demo.kubeconfig and demo1.kubeconfig ~/.kube/
```

### Merged config
```
export KUBECONFIG=~/.kube/demo.kubeconfig:~/.kube/demo2.kubeconfig
kubectl config view --flatten > ~/.kube/config_temp
mv ~/.kube/config_temp ~/.kube/config
```

### Cách sử dụng
```
kubectl config view
kubectl config get-contexts
kubectl config use-context <name context>

```

### ref
```
https://xuanthulab.net/gioi-thieu-va-cai-dat-kubernetes-cluster.html#kubectl
https://docs.bizflycloud.vn/kubernetes_engine/howtos/custom-authentication-authorization-rbac/
https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/
```