# POD

Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.
A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources,
and a specification for how to run the containers. A Pod's contents are always co-located and co-scheduled, and run in a shared context.
A Pod models an application-specific "logical host": it contains one or more application containers which are relatively tightly coupled.
In non-cloud contexts, applications executed on the same physical or virtual machine are analogous to cloud applications executed on the 
same logical host.


  
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

