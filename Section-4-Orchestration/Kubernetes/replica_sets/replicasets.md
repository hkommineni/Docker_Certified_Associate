#### Replica sets
Maintain a stable set of replica pods running at any given time

````sh
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: hkreplicaset
spec:
  replicas: 3
  selector:
    matchLabels:
      tier: frontend-pods
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: gcr.io/google_samples/gb-frontend:v3
````