# YAML in Kubernetes
There are four required fields in a k8s YAML definition.
```yaml
apiVersion:
kind:
metadata:
spec:
```

Example `pod-definition.yaml`
```yaml
apiVersion: v1
kind: Pod
metadata:
    name: myapp-pod
    labels:
        app: myapp
        type: front-end
spec:
    containers:
        - name: nginx-container
          image: nginx
```

Running the above...

```
kubectl create -f pod-definition.yaml
```
