```sh
kubectl taint nodes kubeadm-worker-01 key=value:NoSchedule
```
```sh
kubectl describe node kubeadm-worker-01
```
```sh
kubectl run nginx --image=nginx
```