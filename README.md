Penggunaan di teleport
```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: cluster-admin-to-user-febri4n # Nama ClusterRole yang akan di assign
subjects:
  - kind: User
    name: febri4n # Nama User di teleport
    apiGroup: rbac.authorization.k8s.io
roleRef:
  kind: ClusterRole
  name: cluster-admin # ClusterRole lainnya: admin,view,edit 
  apiGroup: rbac.authorization.k8s.io
```
Apply di cluster
```bash
kubectl apply -f rbac.yaml
```
Teleport solusi alternatif untuk kubectl ke cluster private menggunakan layer 7 loadbalancer

<img width="1269" height="343" alt="image" src="https://github.com/user-attachments/assets/b2ee2373-2b63-4b45-907e-baa49c2427fc" />


