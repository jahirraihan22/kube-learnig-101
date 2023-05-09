# Kubernetes architecture


## NODES

## CLUSTER

## MASTER

## WORKER

## COMPONENTS

- api server
- etcd
  - distributed key value store, store all data use to manage all data
- kubelet
  - The kubelet is the primary "node agent" that runs on each node.
- container runtime
  - manage container like docker
- controller
  - brain of orchestration. manage all of orchestration
- scheduler
  - manage newly created container assign to the nodes

## KUBECTL
  - kubectl controls the Kubernetes cluster manager.
