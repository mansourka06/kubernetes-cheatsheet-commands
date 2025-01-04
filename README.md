# Kubernetes Cheatsheet Commands

This is a comprehensive collection of commonly used Kubernetes commands for managing pods, nodes, deployments, services, and more. Organized for quick reference.

---

## Table of Contents
- [Pod Commands](#pod-commands)
- [Node Commands](#node-commands)
- [Creating Objects](#creating-objects)
- [Monitoring Usage Commands](#monitoring-usage-commands)
- [Deployment Commands](#deployment-commands)
- [Service Commands](#service-commands)
- [Ingress Commands](#ingress-commands)
- [Endpoints Commands](#endpoints-commands)
- [DaemonSet Commands](#daemonset-commands)
- [Job Commands](#job-commands)
- [Rollout Commands](#rollout-commands)
- [Secret Commands](#secret-commands)

---

## Pod Commands
```bash
kubectl get pod                # Get pod
kubectl get pod -o wide         # Get pod wide information
kubectl get pod -w              # Get pod with watch
kubectl get pod -o yaml         # Get pod in YAML format
kubectl edit pod <pod_name>     # Edit pod
kubectl describe pod <pod_name> # Describe pod
kubectl delete pod <pod_name>   # Delete pod
kubectl logs pod <pod_name>     # Logs of the pod
kubectl exec -it pod <pod_name> /bin/bash # Execute into pod
```

## Node Commands
```bash
kubectl describe node <node_name> # Describe node
kubectl get node <node_name>      # Get node
kubectl get node <node_name> -o yaml # Get node in YAML format
kubectl drain node <node_name>    # Drain node
kubectl cordon node <node_name>   # Cordon node
kubectl uncordon node <node_name> # Uncordon node
```

## Creating Objects
```bash
kubectl apply -f <file_name>.yaml                  # Create resource from a file
kubectl apply -f ./<directory_name>               # Create resources from a directory
kubectl apply -f https://<url>                    # Create resource from URL
kubectl run <pod_name> --image=<image_name>       # Create pod
kubectl create deployment <deployment_name> --image=<image_name> # Create Deployment
kubectl create configmap <configmap_name> --from-literal=<key>=<value> # Create ConfigMap
kubectl create secret generic <secret_name> --from-literal=<key>=<value> # Create Secret
```

## Monitoring Usage Commands
```bash
kubectl top node <node_name>  # Get node CPU and memory utilization
kubectl top pods <pod_name>   # Get pod CPU and memory utilization
```

## Deployment Commands
```bash
kubectl get deployment <deployment_name>        # Get Deployment
kubectl describe deployment <deployment_name>   # Describe Deployment
kubectl scale deployment <deployment_name> --replicas=<replicas> # Scale Deployment
```

## Service Commands
```bash
kubectl get service <service>                  # Get Service
kubectl describe service <service>             # Describe Service
kubectl delete service <service>               # Delete Service
```

## Ingress Commands
```bash
kubectl get ingress                             # Get Ingress
kubectl describe ingress <ingress_name>        # Describe Ingress
kubectl delete ingress <ingress_name>          # Delete Ingress
```

## Endpoints Commands
```bash
kubectl get endpoints <endpoints_name>         # Get Endpoints
```

## DaemonSet Commands
```bash
kubectl get daemonset <daemonset_name>         # Get DaemonSet
kubectl describe daemonset <daemonset_name>    # Describe DaemonSet
kubectl delete daemonset <daemonset_name>      # Delete DaemonSet
```

## Job Commands
```bash
kubectl get job <job_name>                     # Get Job
kubectl describe job <job_name>                # Describe Job
kubectl delete job <job_name>                  # Delete Job
```

## Rollout Commands
```bash
kubectl rollout restart deployment <deployment_name>          # Restart Deployment
kubectl rollout undo deployment <deployment_name>             # Undo Deployment to latest revision
kubectl rollout history deployment <deployment_name>          # Get rollout history
```

## Secret Commands
```bash
kubectl get secret <secret_name>               # Get Secret
kubectl describe secret <secret_name>          # Describe Secret
kubectl delete secret <secret_name>            # Delete Secret
```

---

## Contributing
Feel free to contribute by adding more commands or improving the structure. Submit a pull request or open an issue on GitHub.

## License
This project is licensed under the MIT License.

