# argo-oml-manager
Manage OLM Operator with ARGO CD





```
---
apiVersion: operators.coreos.com/v1
kind: OperatorGroup
metadata:
  name: cluster-monitoring
  namespace: cluster-monitoring
  annotations:
    olm.providedAPIs: Alertmanager.v1.monitoring.coreos.com,Prometheus.v1.monitoring.coreos.com,PrometheusRule.v1.monitoring.coreos.com,ServiceMonitor.v1.monitoring.coreos.com
spec:
  staticProvidedAPIs: true
  selector:
    matchLabels:
      something.cool.io/cluster-monitoring: "true"
```      



## Links

  * [https://olm.operatorframework.io/docs/concepts/crds/subscription/](https://olm.operatorframework.io/docs/concepts/crds/subscription/)
  * [https://olm.operatorframework.io/docs/tasks/install-operator-with-olm/#example-install-a-specific-version-of-an-operator](https://olm.operatorframework.io/docs/tasks/install-operator-with-olm/#example-install-a-specific-version-of-an-operator)
  * [https://olm.operatorframework.io/docs/concepts/crds/operatorgroup/](https://olm.operatorframework.io/docs/concepts/crds/operatorgroup/)