# play-k8s-security
- Để đảm bảo an toàn cho hệ thống, k8s dùng giải pháp AAA để bảo mật hệ thống.
  + authentication (chứng thực)
  + authorization (cấp quyền)
  + a...
- Kubernetes as an authentication and authorization server giống với vmware
- authentication : use service account, user account,...
  + Xác thực thông qua username/pass
  + Xác thực thông qua certificate không cần nhập user name và pass
    ví dụ: cấu hình truy cập ssh thông qua certificate.
- authorization : use rbac

- khi tạo user account có hai cách
  + Cách 1: tạo user và pass
  + Cách 2: tạo certificate private key, public key
 
 ### ref
 ```
 https://www.geeksforgeeks.org/computer-network-aaa-authentication-authorization-and-accounting/
 ```
