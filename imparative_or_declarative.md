# IMPERATIVE & DECLARATIVE

## Imperative

- Run the command to generate the definition file:

      kubectl run redis --image=redis:alpine --dry-run=client -oyaml > redis-pod.yaml

- Add given labels ` tier=db ` under the ` metadata ` section.

``` yml

---
apiVersion: v1
kind: Pod
metadata:
  labels:
    tier: db
  name: redis
spec:
  containers:
  - image: redis:alpine
    name: redis
  dnsPolicy: ClusterFirst
  restartPolicy: Always
  
  ```
  
  - Then run the command: ` kubectl create -f redis-pod.yaml` to create the pod from the definition file.
  - OR Use the imperative command:

         kubectl run redis -l tier=db --image=redis:alpine

### Some IMPERATIVE command example

1. create `radis-service` and expose port `6379`
   
        kubectl expose pod redis --port=6379 --name redis-service
    
 2. Create a deployment named `webapp` using the image `kodekloud/webapp-color` with `3` replicas.
        
        kubectl create deployment webapp --image=kodekloud/webapp-color --replicas=3
        
 3. Create a new pod called `custom-nginx` using the `nginx` image and expose it on `container port 8080`.

        kubectl run custom-nginx --image=nginx --port=8080
        
 4. Create a new deployment called `redis-deploy` in the `dev-ns` namespace with the `redis` image. It should have `2` replicas. 

        kubectl create deployment redis-deploy  --image=redis --replicas=2 --namespace=dev-ns
 5. Create a pod called `httpd` using the image `httpd:alpine` in the default namespace. Next, create a service of type `ClusterIP` by the same name `(httpd)`. The target port for the service should be `80`.
   In shortest way.
   
         kubectl run httpd --image=httpd:alpine --port=80 --expose
        
   
   
