# REPLICATION CONTROLLER


## for apiVersion v1

``` yml

apiVersion: v1
kind: ReplicationController
# for apiversion v1 it is ReplicationController
metadata: 
  name: myapp-rc
  labels:
    app: myapp
    type: frontend
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: frontend
    spec:
      containers:
        - name: nginx-container
          image: nginx
  replicas: 3


```

## for apiVersion apps/v1

``` yml

apiVersion: apps/v1
kind: ReplicaSet
metadata: 
  name: myapp-replicaset
  labels:
    app: myapp
    type: frontend
spec:
  template:
    metadata:
      name: myapp-pod
      labels:
        app: myapp
        type: frontend
    spec:
      containers:
        - name: nginx-container
          image: nginx
  replicas: 3
  selector: 
    matchLabels:
      type: frontend

```

#### difference between Replicaset and ReplicationController


