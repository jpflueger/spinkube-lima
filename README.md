# SpinKube for Lima

For commands listed below, make sure to substitute your own preference for resource consumption. 

This template is based on the [examples/k8s.yaml](https://github.com/lima-vm/lima/blob/master/examples/k8s.yaml) from the Lima repository and uses kubeadm to run Kubernetes.

## Virtualization Framework

Create & Start the lima instance:

```shell
limactl start --name=spinkube --cpus=4 --memory=8 ./spinkube-vz.yaml
```

## QEMU

Create & Start the lima instance:

```shell
limactl start --name=spinkube --cpus=4 --memory=8 ./spinkube.yaml
```

## Installing the spin-operator

You still need to install the spin-operator because I didn't want to install Helm on the host VM. 

```shell
helm upgrade --install spin-operator \
  --namespace spin-operator \
  --create-namespace \
  --version 0.1.0 \
  --wait \
  oci://ghcr.io/spinkube/charts/spin-operator
```

## TODOs
- [ ] Add support for local-storage persistent volumes using the /tmp/lima volume mount for services like Redis
