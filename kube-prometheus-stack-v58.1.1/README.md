### Install

```bash
$ helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack --version 58.1.1 \
-f monitor-values.yaml --namespace monitoring
```

### Uninstall

```bash
$ helm uninstall -n monitoring kube-prometheus-stack
```

### Upgrade

```bash
$ helm upgrade kube-prometheus-stack prometheus-community/kube-prometheus-stack --reuse-values -f monitor-values.yaml --namespace monitoring
$ k rollout restart -n monitoring deployment/kube-prometheus-stack-grafana
```

### Slack Alert Install

```bash
$ helm upgrade kube-prometheus-stack prometheus-community/kube-prometheus-stack --reuse-values -f alertmanager-slack.yaml --namespace monitoring
```
