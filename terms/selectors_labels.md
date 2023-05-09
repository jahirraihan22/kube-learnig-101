# SELECTORS & LABELS


- finding selector using pod

      kubectl get pods --selector env=dev
      
- get all selectors including service and replicasets
      
      kubectl get all --selector env=prod
      
- get multiple selctors
      
      kubectl get all --selector env=prod,bu=finance,tier=frontend
