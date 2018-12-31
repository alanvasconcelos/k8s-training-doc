+++
menutitle = "Create a Pod"
date = 2018-12-29T17:15:52Z
weight = 2
chapter = false
pre = "<b>- </b>"
+++

# Create a Coffee App Pod

### Lets Check the running Pods
```
k8s@k8s-master-01:~$ kubectl get pods
No resources found.
k8s@k8s-master-01:~$
```
Nothing <i class="fa fa-frown"></i>

### Lets create one using a `YAML` file
```bash
vi pod.yaml
```

```yml
apiVersion: v1
kind: Pod
metadata:
  name: coffee-app
spec:
  containers:
  - image: ansilh/demo-coffee
    name: coffee
```