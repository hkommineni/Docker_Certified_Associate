#### Deployments

Make use of replicasets and enable the rollout and rollback capabilities.
Benifits:
  Mainting the application revisions by making sure application doesn't go down

#### important pointers
Deployment keeps the history of the revision

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


