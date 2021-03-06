# Kubernetes Utils

## Installation
```bash
$ pip install kubeutils
```

## Usage

Run as `kubeutils [command] [arguments]`.

```
$ kubeutils
kubeutils is a set of Kubernetes utility commands.

Commands:
  ssh              SSH to a pod
  podmaps          Print mapping from pod name to node name

Kubernetes on Google Container Engine (GKE) commands:
  instance-group   Get instance group name for a cluster
  node-count       Get number of nodes in a cluster
```

#### ssh - ssh to a pod.

It's annoying to copy and paste pod names when you want to ssh to a pod. You can use `kubeutils ssh` instead.

```bash
$ kubeutils ssh jup
Multiple pods found:
0) jupyter-john-2
1) jupyter-petko-1
Choice: 0
SSH-ing to jupyter-john-2
root@jupyter-john-2:/# uname -r
4.4.21+
```

#### podmaps - print mapping from pod name to node name.

```bash
$ kubeutils podmaps
hub-1565290413-qmtfc   : gke-jcluster-default-pool-9cc4e660-rx9p
jupyter-john-2         : gke-jcluster-default-pool-9cc4e660-rx9p
jupyter-petko-2        : gke-jcluster-default-pool-9cc4e660-rx9p
```
