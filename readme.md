# Kubernetes Setup Using Ansible and Vagrant
This repository is based on this blog post [Kubernetes blog post on a cluster setup Using Ansible and Vagrant](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/) but it includes some modifications to making it work.

## First Steps After Kubernetes Installation
### Accessing master
```
$ vagrant ssh k8s-master
vagrant@k8s-master:~$ kubectl get no
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   7m42s   v1.17.3
node-1       Ready    <none>   5m4s    v1.17.3
node-2       Ready    <none>   2m33s   v1.17.3

$ tail -f /var/log/syslog
$ kubectl get pods --all-namespaces
```

### Accessing nodes
```
$ vagrant ssh node-1
$ vagrant ssh node-2
```