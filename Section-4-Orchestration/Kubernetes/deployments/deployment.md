#### Deployments

Make use of replicasets and enable the rollout and rollback capabilities.
Benifits:
  Mainting the application revisions by making sure application doesn't go down

#### important pointers
Deployment keeps the history of the revision


#### Create a new deployment
```sh
kubectl create deployment demo-deployment --image=nginx
```
```sh
kubectl get deployment demo-deployment -o yaml
```
#### Set a new image to Deployment
```sh
kubectl set image deployment demo-deployment nginx=httpd
```
#### Edit Deployment
```sh
kubectl edit deployment demo-deployment
```
Set the maxSurge=0

#### Verify the Result
```sh
kubectl set image deployment demo-deployment nginx=httpd
```
```sh
kubectl get pods
```

```sh
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hk-deployments
spec:
  replicas: 5
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: nginx
```

```sh
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hk-deployments
spec:
  replicas: 5
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: nginx:1.23.4
```







