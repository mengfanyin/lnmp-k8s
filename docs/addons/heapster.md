# Heapster

* https://github.com/kubernetes/heapster/tree/master/deploy/kube-config/influxdb

```bash
$ cd deployment/addons/heapster

$ kubectl create -f .

$ kubectl get pods -n kube-system | grep -E 'heapster|monitoring'

$ kubectl cluster-info

$ kubectl proxy --address='172.27.129.105' --port=8086 --accept-hosts='^*$'

$ kubectl get svc -n kube-system|grep -E 'monitoring|heapster'
```

## 删除

```bash
$ kubectl delete service heapster monitoring-grafana monitoring-influxdb -n kube-system

$ kubectl delete deployment heapster monitoring-grafana monitoring-influxdb -n kube-system
```
