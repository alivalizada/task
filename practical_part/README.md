As I have working experience in Kubernetes, I have decided to prepare deployment in it instead of Docker Swarm.

Firstly, we will need to install Kubernetes on local host from official website: https://kubernetes.io/docs/tasks/tools/

Each template can be deployed separately or together:

```kubectl apply -f nginx-configmap.yaml -f nginx-service.yaml -f nginx.yaml -f php-configmap.yaml -f php-service.yaml -f php.yaml```

```
kubectl apply -f nginx-configmap.yaml
kubectl apply -f nginx-service.yaml
kubectl apply -f nginx.yaml
kubectl apply -f php-configmap.yaml
kubectl apply -f php-service.yaml
kubectl apply -f php.yaml
```

In ```nginx.yaml``` and ```php.yaml``` templates, RAM and CPU limits have been configured as below:

```
resources:
limits:
    cpu: 50m
    memory: 50Mi
```

Logs for containers can be accessed by running below commands:

```kubectl get pods```

```kubectl logs <pod-name>```