# zabbix helm

## install KIND

```console
curl -Lo kind https://kind.sigs.k8s.io/dl/latest/kind-linux-amd64
chmod +x kind
sudo mv kind /usr/local/bin/kind
kind --version
```

## create cluster

```console
kind create cluster --name dev --config kind-cluster.yaml
```

## install helm

```console
helm upgrade -i zabbix . -n zabbix --create-namespace
```
