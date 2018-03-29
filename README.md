# kubernetes-yaml

// 创建Deployment
kubectl run nginx --image=nginx
// 创建Service
kubectl expose nginx --port=80 --target-port=8000