# start keybase
# start docker

```sh
traefikeectl install --debug \
    --licensekey=(cat /keybase/private/emilevauge/traefikee-license) \
    --dashboard \
    --kubernetes
```

# dashboard on http://localhost

```sh
kubectl apply -f demo/traefikEE/k8s/cheese-deployments.yaml
kubectl apply -f demo/traefikEE/k8s/cheese-services.yaml
kubectl apply -f demo/traefikEE/k8s/cheese-ingress.yaml
```

# http://cheddar.localhost
# http://stilton.localhost
# http://wensleydale.localhost

```sh
kubectl delete -f demo/traefikEE/k8s/cheese-ingress.yaml
kubectl delete -f demo/traefikEE/k8s/cheese-services.yaml
kubectl delete -f demo/traefikEE/k8s/cheese-deployments.yaml

traefikeectl uninstall --debug
```
