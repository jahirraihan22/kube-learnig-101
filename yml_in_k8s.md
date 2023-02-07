# YAML IN K8s

## Basic yaml structure

``` yaml

apiVersion: v1
kind: Pod
metadata:
  labels: 
    app: frontend-app
    type: frontend-app
  name: my-app
  
spec:
  containers:
    - name: nginx-container
      image: nginx


```

#### apiVersion: 
it can be v1 or apps/v1 etc

#### kind:  
it can be Pod, Replicaset, Service etc (case sensitive) 

#### metadata: 
data about the object like name, label

#### spec: 


## CREATE POD FROM POD DEFINATION YAML

``` yaml

apiVersion: v1
kind: Pod
metadata:
  name: nginx
  labels:
    app: nginx
    tier: frontend
spec: 
  containers:
  - name: nginx
    image: nginx
  # we can use here multiple image

```
  
## SOME COMMANDS FOR PODS


``` sh

      # show all pods
      kubectl get pods
      
      # edit pod defination file
      vim pod.yml
      
      # create pod from pod defination file
      kubectl create -f pod.yml 
      
      # edit  pod from pod defination file
      vim pod.yml
      
      # update after edit pod defination file
      kubectl apply -f pod.yml 
      
      # delete pod
      kubectl delete pod nginx 
      
      #inspect pod
      kubectl describe pods nginx 

```


