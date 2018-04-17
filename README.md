# kubernetes-yaml
https://kubernetes.io/docs/reference/kubectl/cheatsheet/  
https://lms.quickstart.com/custom/858487/LFS258-Labs_V_2018-02-15.pdf  
### Deployment  
kubectl run nginx --image=nginx
kubectl rollout history deployment nginx-deployment
kubectl rollout undo deployment nginx-deployment --to-revision=1
kubectl scale deployment nginx-deployment --replicas=2 
### Service
kubectl expose deployment nginx --type=NodePort --port=80 --target-port=80
### Label
kubectl label nodes <node-name> <label-key>=<label-value>
kubectl get nodes k8s.node1 --show-labels
kubectl get pod --show-labels |grep app=das-cas |awk '{print $1}'