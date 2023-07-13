# dc-k8s-kind
July 2023 DC Kubernetes Meetup


[K8s Kind](https://kind.sigs.k8s.io/)
[K8s Cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

# Create a kind cluster

```
$ kind create cluster --config=/foo/bar/config.yaml
$ k cluster-info --context foobar
```

# Some aliases 
```
alias kgp="kubectl get pods"
alias kgn="kubectl get nodes"
alias kdp="kubectl describe pods"
alias kdn="kubectl describe nodes"
alias kpl="kubectl get pods -o yaml"
alias ka="kubectl apply -f "
alias kd="kubectl delete -f "
alias ks="kubectl config use-context "
alias kn='kubectl config set-context --current --namespace '
alias cl="awk "NF" "
export do="--dry-run=client -o yaml"
export now="--force --grace-period=0"
export l="-o yaml"
export w="kubectl run tmp --restart=Never --rm -i --image=nginx:alpine -- curl -m 5 "
```

# Build and load a container 

```
$ docker build -t demo:v0.1 .
```
```
$ kind load docker-image demo:v0.1
```