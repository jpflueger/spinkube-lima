# SpinKube for Lima

For commands listed below, make sure to substitute your own preference for resource consumption. 

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
