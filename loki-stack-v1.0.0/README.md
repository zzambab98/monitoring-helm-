### Install

```bash
$ helm dependency build
$ helm install loki-stack . -f values.yaml --namespace monitoring
$ k rollout restart -n monitoring daemonset/loki-stack-promtail
```

### Uninstall

```bash
$ helm dependency update .
$ helm uninstall loki-stack -n monitoring
```

### Upgrade

```bash
$ helm upgrade loki-stack . -n monitoring -f ./values.yaml
$ k rollout restart -n monitoring daemonset/loki-stack-promtail
```

### Debug

```bash
$ helm install loki-stack . -f values.yaml --namespace monitoring --dry-run=server --debug
```
